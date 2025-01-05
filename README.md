

# DMARC Dashboard

The **DMARC Dashboard** is a web-based tool designed to parse and visualize DMARC and forensic reports. It offers a comprehensive interface for monitoring domain-level email authentication metrics, including SPF, DKIM, and alignment rates. 

This repository contains the necessary configuration files to set up and deploy the DMARC Dashboard using Docker.

---

## Key Features

- **Visualization**: Interactive charts and tables to analyze DKIM, SPF pass rates, alignment rates, and message volume trends.
- **Authentication Analysis**: Detailed failure analysis, common issues, and source IP reports.
- **Domain Management**: Compare metrics across multiple domains and time periods.
- **Automation**: Automatically fetch and parse DMARC reports via IMAP.

---

## Getting Started

Follow the steps below to deploy the DMARC Dashboard on your system.

### Prerequisites

- Docker and Docker Compose installed on your system.
- Access to DMARC and forensic email accounts for the domains you want to monitor.
- A `.env` file containing configuration details for each domain.

---

### Clone the Repository

```bash
git clone https://github.com/riazsomc/dmarc-dashboard.git
cd dmarc-dashboard
```

---

### Configure Environment Variables

Edit the `.env` file in the working directory with the following format:

```dotenv
# Domain 1 Configuration
DOMAIN1_NAME=example.com
DOMAIN1_DMARC_EMAIL=dmarc@example.com
DOMAIN1_DMARC_IMAP_SERVER=imap.example.com
DOMAIN1_DMARC_IMAP_USERNAME=dmarc@example.com
DOMAIN1_DMARC_IMAP_PASSWORD=your-password
DOMAIN1_FORENSIC_EMAIL=forensic@example.com
DOMAIN1_FORENSIC_IMAP_SERVER=imap.example.com
DOMAIN1_FORENSIC_IMAP_USERNAME=forensic@example.com
DOMAIN1_FORENSIC_IMAP_PASSWORD=your-password

# Domain 2 Configuration
DOMAIN2_NAME=anotherdomain.com
DOMAIN2_DMARC_EMAIL=dmarc@anotherdomain.com
DOMAIN2_DMARC_IMAP_SERVER=imap.anotherdomain.com
DOMAIN2_DMARC_IMAP_USERNAME=dmarc@anotherdomain.com
DOMAIN2_DMARC_IMAP_PASSWORD=your-password
DOMAIN2_FORENSIC_EMAIL=forensic@anotherdomain.com
DOMAIN2_FORENSIC_IMAP_SERVER=imap.anotherdomain.com
DOMAIN2_FORENSIC_IMAP_USERNAME=forensic@anotherdomain.com
DOMAIN2_FORENSIC_IMAP_PASSWORD=your-password
```

> Add additional domains by following the same format.

---

### Deploy the Application

1. **Run Docker Compose**:
   ```bash
   docker-compose up -d
   ```

2. **Access the Dashboard**:
   Open your browser and navigate to `http://localhost`.

---

### Folder Structure

```
dmarc-dashboard/
│
├── .env        # Configuration file with domain-specific settings
│           
├── docker-compose.yml  # Docker Compose configuration
```

---

## Contribution

Contributions are welcome! Please feel free to submit a pull request or open an issue to discuss potential improvements.

---

## License

This project is licensed under the MIT License.

---

If you have any questions or need help with the setup, feel free to create an issue in the repository.

--- 