# NBA ADP Player Selector - README

## Overview

The **NBA ADP Player Selector** is a web-based tool that helps users select NBA players based on their Average Draft Position (ADP) across multiple platforms. The tool allows users to input a player's name and view the player’s ADP data from different fantasy sports platforms. Users can pick players, which removes them from the available list, and their selections are logged in a history for easy reference.

The data for player ADPs is retrieved from a CSV file (nba-adp-All.csv) that contains the ADP data from various platforms such as ESPN, CBS, Yahoo, Underdog, and Fantrax. The tool calculates the average ADP across these platforms to help users identify the best available players.

---

## Features

1. **Player Selection**: Users can input a player’s name from a list of available NBA players, and the player will be added to their selection history.
2. **Best Available Player**: The tool dynamically calculates the best available player based on the average ADP from multiple platforms.
3. **Pick History**: All selected players are logged and displayed in a list with their ADP data.
4. **Interactive UI**: The user-friendly interface allows players to be picked and updated in real-time.
5. **Data Source**: The player data is pulled from a CSV file containing ADP information from multiple sources.

---

## Files and Resources

### `index.html`
- The main HTML file containing the structure of the NBA ADP Player Selector interface.
- Uses the **PapaParse** library for parsing the CSV data.
- Contains input fields, buttons, and containers for displaying the available players and pick history.

### `nba-adp-All.csv`
- The CSV file that contains the ADP data for NBA players from different fantasy sports platforms (ESPN, CBS, Yahoo, Underdog, Fantrax).
- Data includes columns: `Name`, `AVG`, `ESPN`, `CBS`, `Yahoo`, `Underdog`, `Fantrax`.

---

## How It Works

1. **Loading the CSV**: 
    - When the page loads, the CSV file `nba-adp-All.csv` is parsed using the PapaParse library.
    - The data is stored in a JavaScript object where each player’s ADP values from different platforms are stored.

2. **Player Input**:
    - Users type in a player's name in the text field and click the "Pick Player" button to select the player.
    - The selected player is removed from the list of available players and is added to the player's pick history.

3. **Best Available Player**:
    - The tool calculates the average ADP for all available players and displays the best available player with the lowest average ADP.
    - The ADP data from different platforms is displayed for each player for transparency.

4. **Pick History**:
    - Once a player is picked, it is logged in the "Pick History" section for the user to reference.

---

## Data Structure

The data in the CSV file is expected to have the following structure:

| Name      | AVG  | ESPN  | CBS  | Yahoo  | Underdog  | Fantrax  |
|-----------|------|-------|------|--------|----------|----------|
| Player 1  | 12.4 | 15    | 10   | 14     | 11       | 13       |
| Player 2  | 23.6 | 20    | 25   | 22     | 23       | 24       |
| ...       | ...  | ...   | ...  | ...    | ...      | ...      |

- `Name`: The name of the NBA player.
- `AVG`: The average ADP across all platforms.
- `ESPN`, `CBS`, `Yahoo`, `Underdog`, `Fantrax`: The ADP values from respective fantasy sports platforms.

---

## Usage

1. **Enter Player Name**: Type the name of a player into the input field.
2. **Pick Player**: Click the **"Pick Player"** button to select a player. The player will be removed from the available players list and added to the pick history.
3. **Best Available Player**: The best available player (with the lowest average ADP) is displayed dynamically on the page.
4. **View Pick History**: See the history of players selected in the "Pick History" section, which will list all previously picked players along with their ADP data.

---

## Technologies Used

- **HTML5**: For the structure of the web page.
- **CSS3**: For styling the layout and ensuring responsiveness.
- **JavaScript**: For the core functionality such as handling player input, updating the best player, and maintaining the pick history.
- **PapaParse**: For parsing the CSV data in the browser.

---

## How to Run

To use the NBA ADP Player Selector locally:

1. Ensure you have the following files:
   - `index.html`
   - `nba-adp-All.csv` (with the correct format as described above)

2. Open the `index.html` file in any modern web browser (Google Chrome, Mozilla Firefox, Safari, etc.).

3. Once the page is loaded, the data will be fetched and displayed.

---

## Troubleshooting

- **CSV file not found**: Make sure the `nba-adp-All.csv` file is placed in the same directory as the HTML file. If the file is not accessible, the player list will not load.
  
- **Player not found**: Ensure that the player's name is typed exactly as it appears in the CSV file. The input is case-sensitive.

- **No players available**: If the CSV file has no valid player data or all players have been picked, the message "No players available" will be shown.

---

## License

This project is open-source and free to use. No attribution is required, but feel free to customize or expand upon the project for your own purposes.

---

## Acknowledgements

- **PapaParse**: For the excellent CSV parsing library used to handle and parse CSV files in the browser.
