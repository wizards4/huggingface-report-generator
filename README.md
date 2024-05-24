# HuggingFace Report Generator

This Docker container periodically generates reports by fetching data from the Hugging Face model hub, compiling a list of the top 10 downloaded models, and then stopping the container.

## Requirements

- Docker

## Setup

1. Clone the repository:
    ```sh
    git clone https://github.com/your-username/huggingface-report-generator.git
    cd huggingface-report-generator
    ```

2. Build the Docker image:
    ```sh
    docker build -t huggingface-report-generator .
    ```

3. Run the Docker container:
    ```sh
    docker run --rm -v $(pwd)/reports:/usr/src/app huggingface-report-generator
    ```

   The report will be saved to the `reports` directory in the current working directory.

## Scheduling

To run the container periodically, you can set up a cron job on your Linux machine. For example, to run the container daily at midnight, add the following line to your crontab (edit it using `crontab -e`):

