# Drifter

Drifter is a lightweight, Go-based tool designed to detect and remediate configuration drifts in your AWS infrastructure. This tool helps maintain consistency across your cloud resources, ensuring that they align with predefined baselines.

---

## Scope
Drifter focuses on identifying and correcting configuration deviations across various AWS resources, including:

- **EC2 Instances**:
  - Detecting changes in instance types, tags, monitoring states, IAM roles, and more.
  - Restoring configurations to match baselines.

- **Security Groups**:
  - Identifying overly permissive or unauthorized rules.
  - Automatically reverting rules to the intended configuration.

- **EBS Volumes**:
  - Detecting changes in volume size or type.
  - Modifying volumes to comply with baselines.

- **Other AWS Resources (Future Support)**:
  - S3 bucket policies.
  - IAM roles and policies.
  - DynamoDB and other services as needed.

---

## Key Features
- **Drift Detection**:
  - Compares current AWS resource configurations against baselines stored in YAML/JSON or a version control system (e.g., Git).

- **Automated Remediation**:
  - Fixes detected drifts by leveraging the AWS SDK for Go.

- **Extensibility**:
  - Designed to add support for more AWS services easily.

- **Reporting**:
  - Outputs detailed logs and optionally sends notifications about detected and resolved drifts.

---

## Why Use Drifter?
Managing AWS infrastructure at scale can lead to accidental or intentional configuration changes. Drifter:
- Enhances security by detecting drifts like overly permissive security group rules.
- Saves time by automating routine tasks like fixing mismatched instance configurations.
- Helps maintain compliance with organizational policies or industry standards.

---

## Getting Started
### Prerequisites
- **AWS Credentials**:
  Ensure you have configured your AWS CLI with the appropriate access permissions.

- **Go Installed**:
  Install Go by following the [official Go installation guide](https://go.dev/doc/install).

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/drifter.git
   ```
2. Navigate to the project directory:
   ```bash
   cd drifter
   ```
3. Build the project:
   ```bash
   go build -o drifter
   ```

### Usage
Run Drifter to detect and remediate drifts:
```bash
./drifter --config baseline.yaml
```

Options:
- `--config`: Path to the baseline configuration file.
- `--dry-run`: Run the tool without making changes, just to detect drifts.
- `--log-level`: Set the verbosity of logs (e.g., `info`, `debug`).

---

## Roadmap
- **Service Expansion**: Add support for more AWS resources like S3, RDS, and IAM policies.
- **Web Dashboard**: A web interface for monitoring and managing drifts.
- **Custom Rules**: Allow users to define additional validation rules.

---

## Contributing
We welcome contributions! Please see our [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## License
Drifter is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---

## Acknowledgments
- Built with ❤️ by cloud enthusiasts.
- Inspired by real-world challenges in maintaining cloud infrastructure consistency.

---

Start keeping your AWS infrastructure in sync with **Drifter**!

