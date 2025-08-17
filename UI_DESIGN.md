# Video Downloader App: UI/UX Design Proposal

## 1. Design Philosophy

This design is guided by four core principles to ensure a best-in-class user experience.

*   **Mobile-First:** The interface is designed for the smallest screens first, ensuring a seamless experience on any device. The layout is clean, and touch targets are large and accessible.
*   **Simplicity & Speed:** The primary user journey—pasting a link and starting a download—is optimized to be as fast and frictionless as possible. The UI is uncluttered, intuitive, and guides the user naturally.
*   **Trustworthy & Transparent:** The app communicates clearly what's happening at every step. Detailed download progress, clear error messages, and transparent options build user confidence and trust.
*   **Power on Demand:** Advanced features are available for power users but are kept out of the way of the primary workflow, preventing overwhelm for new users.

---

## 2. Screen-by-Screen Breakdown

### Screen 1: Home (Paste Link)

This is the user's entry point. The goal is to get them to initiate a download with minimal effort.

**Layout & Components:**

*   **Header:** Contains the app logo/name ("Downloader") and a subtle settings icon (cogwheel) on the right.
*   **URL Input Field:** A large, prominent text input field with clear placeholder text: `Paste video link here`.
    *   **Interaction:** When the user taps the field, the border could subtly glow with the primary brand color.
*   **Paste from Clipboard Button:** Below the input field, a button labeled `Paste from Clipboard` appears if a valid URL is detected in the clipboard. This is a major UX enhancement.
*   **Primary CTA Button:** A full-width button at the bottom of the screen labeled `Fetch Media`. It is disabled by default and becomes active once a valid URL is entered.
*   **Bottom Navigation:** A simple tab bar with two icons: **Home** (active) and **Downloads**.

**Visual Mockup Idea:**

```
+------------------------------------------+
| Downloader                      ⚙️      |
+------------------------------------------+
|                                          |
|   [ Paste video link here              ] |
|                                          |
|   ( intelligente Paste from Clipboard )   |
|                                          |
|                                          |
|                                          |
|   +------------------------------------+   |
|   |           Fetch Media            |   |
|   +------------------------------------+   |
|                                          |
+------------------------------------------+
|   🏠 Home          📥 Downloads         |
+------------------------------------------+
```

---

### Screen 2: Media Selection

After fetching the URL, this screen presents the available download options in a clear, organized manner.

**Layout & Components:**

*   **Header:** Displays a thumbnail of the video and its title, confirming to the user they've pasted the correct link. A "Back" button is on the left.
*   **Format Tabs:** "Video" and "Audio" tabs allow users to easily switch between media types, preventing a cluttered list.
*   **Download Options List (Video Tab):**
    *   Each list item represents a different quality and includes:
        *   **Resolution:** e.g., `1080p`, `720p`
        *   **File Size:** e.g., `150 MB`
        *   **Format:** e.g., `MP4`
        *   **Download Icon:** A clear download icon/button on the right.
*   **Download Options List (Audio Tab):**
    *   Similar to the video list, but for audio formats:
        *   **Quality:** e.g., `High (128kbps)`
        *   **File Size:** e.g., `4.5 MB`
        *   **Format:** e.g., `M4A`
*   **Advanced Controls (Optional):** A small "Advanced" or "More Options" toggle could reveal settings like subtitle downloads or different file containers (MKV, WEBM) without cluttering the primary view.

**Visual Mockup Idea:**

```
+------------------------------------------+
| <   Video Title Goes Here...             |
+------------------------------------------+
|                                          |
|   [ Video Thumbnail ]                    |
|                                          |
|   +----------+ +-----------+             |
|   |  Video   | |   Audio   |             |
|   +----------+ +-----------+-------------+
|                                          |
|   1080p  MP4         150 MB     (↓)      |
|   -------------------------------------- |
|   720p   MP4         85 MB      (↓)      |
|   -------------------------------------- |
|   480p   MP4         45 MB      (↓)      |
|                                          |
+------------------------------------------+
|   🏠 Home          📥 Downloads         |
+------------------------------------------+
```

---

### Screen 3: Downloads

This screen provides a centralized hub for managing all ongoing and completed downloads.

**Layout & Components:**

*   **Header:** Titled "Downloads".
*   **Status Tabs:** "In Progress" and "Completed" tabs to organize the download list.
*   **"In Progress" List:**
    *   Each item shows:
        *   Video thumbnail and title.
        *   A progress bar with percentage.
        *   Download speed (`2.5 MB/s`) and file size (`45 MB / 150 MB`).
        *   Controls to **Pause**, **Resume**, and **Cancel**.
*   **"Completed" List:**
    *   A list of successfully downloaded files.
    *   Each item shows:
        *   Thumbnail and title.
        *   File size and duration.
        *   Action buttons: **Play**, **Share**, **Delete**.

**Visual Mockup Idea:**

```
+------------------------------------------+
| Downloads                                |
+------------------------------------------+
|   +-------------+ +-------------+        |
|   | In Progress | |  Completed  |        |
|   +-------------+ +-------------+--------+
|                                          |
|   [Thumb] Video Title 1                  |
|   [|||||||||-- 68% --]  45/150MB          |
|   2.5 MB/s          (❚❚)  (X)           |
|   -------------------------------------- |
|   [Thumb] Video Title 2                  |
|   [|||-------- 20% --]  12/60MB           |
|   1.8 MB/s          (❚❚)  (X)           |
|                                          |
+------------------------------------------+
|   🏠 Home          📥 Downloads         |
+------------------------------------------+
```

---

### Screen 4: Settings

Accessible from the Home screen, this area houses app-level configurations.

**Layout & Components:**

*   A standard, clean settings list.
*   **Download Folder:** Choose where to save files.
*   **Max Concurrent Downloads:** Slider or dropdown (e.g., 1-5).
*   **Wi-Fi Only:** A toggle switch to restrict downloads to Wi-Fi networks.
*   **Appearance:** Options for Light, Dark, or System theme.
*   **Notifications:** Manage download completion/failure alerts.
*   **Help & Feedback:** Links to support, FAQs, and a feedback form.
*   **About:** App version and license information.

---

## 3. Visual Design System

*   **Color Palette:**
    *   **Primary:** A deep, modern blue (`#0052FF`) for buttons, active states, and headers.
    *   **Neutrals:**
        *   Background: A very light grey (`#F5F5F7`) to be easy on the eyes.
        *   Text: A dark grey (`#1D1D1F`) for readability.
        *   Borders/Dividers: A light grey (`#E0E0E0`).
    *   **Accents:**
        *   **Success:** A vibrant green (`#34C759`) for completed statuses.
        *   **Error:** A clear red (`#FF3B30`) for failed downloads or errors.
*   **Typography:**
    *   **Font:** **Inter**. It's a clean, highly readable sans-serif font that works well for UI.
    *   **Hierarchy:**
        *   **Headings:** Bold, 24pt.
        *   **Subheadings/Titles:** Semi-Bold, 18pt.
        *   **Body/Labels:** Regular, 16pt.
*   **Iconography:**
    *   **Style:** Use a consistent, modern, and lightweight icon set like **Feather Icons**. This contributes to a clean and professional aesthetic.

---

## 4. User Flow Summary

1.  **Open App:** User lands on the **Home** screen.
2.  **Paste Link:** User pastes a video link into the input field.
3.  **Fetch Media:** User taps the `Fetch Media` button. A loading indicator appears.
4.  **Select Quality:** The app navigates to the **Media Selection** screen. User taps the download icon for their desired quality (e.g., `720p`).
5.  **Monitor Download:** The download begins, and the user is automatically taken to the **Downloads** screen (In Progress tab), where they can see the live progress.
6.  **Download Complete:** The item moves from "In Progress" to the "Completed" tab. A notification may appear.
7.  **Manage File:** The user can now play, share, or delete the downloaded file from the "Completed" list.
