# Cloud Custodian Policies for Key Performance Indicators (KPIs)

This repository contains Cloud Custodian policies aimed at monitoring and managing various Key Performance Indicators (KPIs) within your cloud environment. Each policy is designed to address specific KPIs for better cost management, resource optimization, and compliance.

Below is a description of each KPI along with the Cloud Custodian policy associated with it:

### RI Coverage
- **Description:** Ensures coverage of Reserved Instances (RIs) and identifies instances running on-demand without RI coverage.
- **Policy:** `ensure-ri-coverage.yaml`

### Savings Plan Coverage
- **Description:** Monitors on-demand instances without Savings Plan coverage and marks them for action after a specified period.
- **Policy:** `ensure-savings-plan-coverage.yaml`

### Committed Use Discount Coverage
- **Description:** Tracks utilization of committed use discounts on Google Cloud Platform instances.
- **Policy:** `ensure-committed-use-discount-coverage.yaml`

### Rightsizing Opportunity Value
- **Description:** Identifies instances with excessive CPU/Memory, suggesting rightsizing opportunities.
- **Policy:** `identify-rightsizing-opportunities.yaml`

### Usage on Weekends vs Weekdays
- **Description:** Monitors usage patterns, distinguishing between weekends and weekdays.
- **Policy:** `monitor-usage-pattern.yaml`

### % of Spot vs Other Coverage
- **Description:** Analyzes the percentage of Spot Instances compared to other instance types.
- **Policies:** `calculate-spot-instances.yaml`, `calculate-non-spot-instances.yaml`

### Custom Pricing Commitment Tracking
- **Description:** Monitors the utilization of custom pricing commitments.
- **Policy:** `track-custom-pricing-commitment.yaml`

### % Orphaned EBS Volumes
- **Description:** Identifies and alerts on orphaned Elastic Block Store (EBS) volumes.
- **Policy:** `identify-orphaned-ebs-volumes.yaml`

### % Orphaned Snapshots
- **Description:** Detects and notifies about orphaned snapshots.
- **Policy:** `identify-orphaned-snapshots.yaml`

### Aged Snapshots
- **Description:** Monitors snapshots older than a specified threshold.
- **Policy:** `identify-aged-snapshots.yaml`

... (and so on for each KPI)

For detailed implementation and configuration of each policy, refer to the respective YAML files in this repository.

## Usage
- Clone this repository to your local environment.
- Adjust policy parameters (thresholds, actions, notifications) as needed in the YAML files.
- Deploy Cloud Custodian with these policies in your cloud environment for automated monitoring.

### Example Command to Run Cloud Custodian
```
custodian run --output-dir output_folder policy_file.yaml
```

### Note
- Always test policies in a non-production environment before applying them to your production setup.
- Customize policies to suit your specific cloud environment, KPIs, and compliance requirements.

