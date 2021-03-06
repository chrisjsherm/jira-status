## JiRA Status
### Python module for collecting information on a JiRA project.

## Table of Contents

* [Configuration](#configuration)
* [Usage](#usage)
* [Options](#options)
* [Send Email](#send-an-email)
* [License](#license)

## Configuration

Rename the `sample.configuration.json` to `configuration.json` and enter the configuration values.

If you're using [Anaconda](//anaconda.org/) to manage your Python environment,
run the following command from the root of the repository to create an
environment with the necessary dependencies.
```bash
conda config --add channels conda-forge
conda create --name jira_status --file requirements.txt
```

## Usage

```bash
python .\jira-status\ --verbose
```

You can find the output of the script in the `logs` directory of the project.

## Options

Option | Description | Usage
---    | ---         | ---
Verbose | Outputs the status and information about the script's progress to the CLI. | `--verbose`

## Send an Email

You can utilize the `send-email.py` module to send an email message via Office 365.

```bash
python .\jira-status\send-email.py -f .\jira-status\logs\status.html -html --verbose
```

Option | Description | Usage
---    | ---         | ---
File | File containing the email body. | `-f`
HTML | Send the email as HTML instead of plain text. | `-html`
Verbose | Outputs the status and information about the script's progress to the CLI. | `--verbose`

## License

MIT