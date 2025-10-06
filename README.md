# Smart Invoice & Billing Application

## Overview

The **Smart Invoice & Billing Application** is a professional, single-page application (SPA) designed for managing client data, creating invoices, tracking billing status, and generating reports. Built using React and styled with Tailwind CSS, this application provides a responsive, real-time solution for small business financial management.

Data persistence and real-time synchronization are handled robustly using **Google Firebase Firestore**.

## Features

This application is designed to offer a complete solution for core business billing processes:

* **Real-time Dashboard:** Provides a clear, data-driven overview of key financial metrics using **Chart.js** for effective visualization.
* **Invoice Management:** Full CRUD (Create, Read, Update, Delete) functionality for managing detailed client invoices.
* **Client Management:** A dedicated section to maintain and reference customer and client information.
* **PDF Reporting:** Generate professional and printable invoice and summary PDF documents directly within the browser using **jsPDF** and **Autotable**.
* **Global Search:** Instant, predictive search capabilities across all clients and invoices for quick data retrieval.
* **Data Persistence:** Uses **Firebase Firestore** for secure, multi-user data storage and synchronization.
* **Modern UI/UX:** A fully responsive, dark-themed interface built with **Tailwind CSS** ensuring optimal use on desktop, tablet, and mobile devices.

---

## Technology Stack

The application leverages a modern, efficient, and lightweight stack:

| Category | Technology | Purpose |
| :--- | :--- | :--- |
| **Frontend Framework** | React (via Babel) | Component-based UI development and state management. |
| **Styling** | Tailwind CSS | Utility-first framework for responsive and modern design. |
| **Database & Auth** | Firebase Firestore & Auth | Real-time, scalable data storage and secure user authentication. |
| **Charting** | Chart.js | Rendering interactive and dynamic charts for the dashboard. |
| **PDF Generation** | jsPDF / Autotable | Client-side generation of professional PDF documents. |
| **Bundling/Execution** | Single `index.html` | Self-contained file for easy deployment and portability. |

---

## Setup and Running

Since this project is a single, self-contained HTML file running in a Canvas environment, no complex installation steps are required.

### Canvas Environment Instructions

1.  **Load the File:** Ensure the `index.html` file is loaded into the provided development environment.
2.  **Authentication:** The application will automatically attempt to authenticate using the provided Canvas environment tokens (`__initial_auth_token`) or fall back to anonymous sign-in to ensure immediate access to the Firestore database.
3.  **Start Using:** Once the app initializes (indicated by the dashboard load), you can begin creating clients and generating invoices.

### Data Storage & Security

Data is stored securely in Firebase Firestore under the following path structure, utilizing the Canvas-provided `__app_id` and user authentication (`userId`):

* **Private Data:** `/artifacts/{__app_id}/users/{userId}/invoices`
* **Private Data:** `/artifacts/{__app_id}/users/{userId}/clients`

---

## Usage

The primary interaction flow involves using the navigation sidebar to switch between views:

1.  **Dashboard:** Review graphical summaries and key performance indicators.
2.  **Clients:** Add new clients or edit existing client details.
3.  **Invoices:** Create a new invoice, associating it with an existing client, and then view, edit, or mark its status (e.g., Paid, Pending).
4.  **PDF Export:** Click the appropriate button (e.g., "Generate PDF") from an invoice detail view to instantly create and download the document.
