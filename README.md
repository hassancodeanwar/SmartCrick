# SmartCrick




![image](https://github.com/user-attachments/assets/73fa6212-2638-429e-b764-1e5816d176fe)


<aside>
<img src="/icons/document_yellow.svg" alt="/icons/document_yellow.svg" width="40px" />

# 🧩 Problem Statement

Automated Cricket Video Analysis System Utilizing Computer Vision

**Background:**

In cricket, performance analysis often requires manual review of hours of match footage to evaluate player techniques, shot types, and key events. This is time-consuming and prone to human error, especially when trying to gather statistics on player strengths, weaknesses, and dismissals. With advancements in computer vision and deep learning, it's possible to automate this process for faster, more accurate insights.

**Problem:**

There is no accessible, automated system that can detect players and ball movement, classify shot types, and generate insights and highlights from raw cricket footage, especially in varied video conditions. Analysts and coaches need a tool that can process videos efficiently and provide actionable performance metrics.

**Objective:**

To develop a computer vision-based system that detects players and ball movement in cricket videos, classifies shot types, tracks performance, and automatically generates highlight clips, enabling deeper player analysis with minimal manual effort.

</aside>

<aside>
<img src="/icons/document_yellow.svg" alt="/icons/document_yellow.svg" width="40px" />

## 📄 Software Requirements Specification (SRS)

### 1. **Introduction**

**1.1 Purpose**

This document defines the software requirements for an automated cricket video analysis system. It provides details on functionality, interfaces, and design constraints for developing a solution that extracts meaningful analytics from cricket match footage using computer vision techniques.

**1.2 Scope**

The software will detect players and balls in cricket footage, classify shots, track outcomes, and generate performance metrics and highlight clips. It will provide APIs to integrate with a frontend dashboard for coaches, analysts, and players.

**1.3 Definitions**

- **Shot Classification**: Identifying the type of batting shot played (e.g., pull, drive).
- **Object Tracking**: Monitoring the movement of players and the ball across frames.
- **Highlight Generation**: Extracting short video clips around detected key actions.

---

### 2. **Overall Description**

**2.1 Product Perspective**

This product acts as the backend for a broader analytics platform and integrates with an existing or upcoming frontend UI. It will be deployed on a cloud platform and will accept video uploads via API.

**2.2 Product Functions**

- Upload and preprocess cricket videos.
- Detect players and the ball in a video.
- Track player and ball movement.
- Classify each batting shot.
- Record outcomes (e.g., runs scored, dismissals).
- Generate highlight clips for each shot.
- Store processed video data and statistics.
- Provide APIs to retrieve insights and clips.

**2.3 User Classes and Characteristics**

- **Analysts**: Access player insights and video clips.
- **Coaches**: Use insights for training and strategy.
- **Players**: Review their performance.
- **Developers**: Integrate the API into the frontend.

**2.4 Constraints**

- Must run efficiently on cloud infrastructure.
- Should support variable video quality and formats.
- Must ensure secure video upload and data storage.

---

### 3. **Specific Requirements**

### 3.1 Functional Requirements

- **FR1**: The System shall accept video uploads via REST API.
- **FR2**: The System shall detect and track players and the ball in all video frames.
- **FR3**: The System shall classify shot types from batting footage.
- **FR4**: System shall detect shot outcomes (e.g., boundary, wicket).
- **FR5**: The System shall generate short video highlights per shot.
- **FR6**: System shall store metadata (player name, shot type, outcome).
- **FR7**: System shall provide APIs for querying player stats and highlights.

### 3.2 Non-Functional Requirements

- **NFR1**: Accuracy of detection and classification ≥ 85%.
- **NFR2**: Processing time ≤ 15 minutes for a 1-hour video.
- **NFR3**: Scalability to handle 5–10 matches daily.
- **NFR4**: API response times < 2 seconds.
- **NFR5**: System must encrypt stored videos and secure API access.

### 3.3 External Interface Requirements

- **User Interface**: Integrates with existing frontend.
- **API Interface**: RESTful endpoints for video upload and data access.
- **Hardware Interface**: Supports cloud GPUs (e.g., NVIDIA T4, A100).
- **Software Interface**: Uses TensorFlow/PyTorch, OpenCV, FFmpeg, Docker.
</aside>
