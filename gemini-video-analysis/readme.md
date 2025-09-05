# Gemini Video Metadata Generator

This repository contains a Google Colab notebook that demonstrates how to use the Gemini API to analyze a video file stored in Google Cloud Storage (GCS). The script generates a detailed, time-based metadata log of all significant events, scenes, and actions.

This is useful for quickly understanding a video's content or for building applications that allow users to search for specific moments within a video.

---

## Features

* Analyzes video content using the multimodal capabilities of the Gemini model (`gemini-2.5-flash`).
* Processes a video directly from a GCS URI, eliminating the need for local downloads.
* Generates a structured, time-stamped log of events and actions.
* Outputs the metadata as a clean Markdown table.
* Displays the token usage for the API request and response.

---

## Prerequisites

Before running the notebook, you will need:

* A Google Cloud Project with the **Vertex AI API** enabled.
* A video file uploaded to a Google Cloud Storage (GCS) bucket.
* Authentication credentials configured for your environment. (The notebook handles this automatically if run in Google Colab).

---

## How to Use

1.  Open the `Gemini-Video-Analysis.ipynb` notebook in Google Colab.
2.  Update the `PROJECT_ID` variable in the first code cell with your Google Cloud Project ID.
3.  Modify the `gcs_video_uri` variable to point to the path of your video file in GCS (e.g., `gs://your-bucket-name/your-video.mp4`).
4.  Run the notebook cells in order by selecting **Runtime > Run all**.

---

## Example Output

The script will output a Markdown table containing the analysis. The format will look similar to this:

```text
| Timestamp (MM:SS) | Description                                       | Player Name   | Action | Keywords                      |
|-------------------|---------------------------------------------------|---------------|--------|-------------------------------|
| 00:00             | LeBron James executes a powerful dunk...          | LeBron James  | Dunk   | Alley-oop, Powerful, Timeout  |
| 00:06             | Lakers player receives a pass under the basket... | Anthony Davis | Layup  | Assist, Under basket, Fluid   |
| ...               | ...                                               | ...           | ...    | ...                           |