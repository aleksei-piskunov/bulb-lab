# bulb-lab
An interactive playground for experimenting with a row-and-column light bulb puzzle. Try move sequences, compare successful attempts, and explore different grid sizes. The site is an experimental tool: it does not provide an optimal solution or prove that a sequence is minimal.

## The puzzle

An 8 × 8 grid contains 64 light bulbs, all initially off. In one move, choose a cell and toggle every bulb in its row and column: an off bulb turns on, and an on bulb turns off. The selected bulb, where the row and column intersect, is toggled **only once**.

**What is the minimum number of moves required to turn all 64 bulbs on?**

The simulator starts with the original 8 × 8 grid. It also supports rectangular grids with 1–30 rows and 1–30 columns for further experiments, using the same move rule and goal.

## Run locally

Download or clone this repository and open `index.html` in a web browser. No installation, build step, server, or internet connection is required. All styles and JavaScript are included in that file.

## How to use it

- Choose the number of rows and columns, then select **New grid**.
- Click a bulb to make a move. The move counter and current path update automatically.
- Select **Undo move** to undo the last move in an unfinished attempt, or **Reset** to start over.
- When all bulbs are on, the successful attempt is saved with its grid size, move count, timestamp, and full path.
- Automatic reset after success is enabled by default. Turn it off to inspect the completed grid.
- Select **Replay step by step** beside a saved result to inspect it. Your current attempt is restored when you leave replay.
- Select **Download path** or **Download all results** to export JSON files.

Coordinates are written as **(row, column)**, starting at **(1, 1)** in the top-left corner. A path lists clicks in the order they were made.

## History and privacy

Successful attempts are stored locally using `localStorage`. History belongs to the browser profile and site origin; it is not shared between visitors or synchronized across devices. People using the same browser profile share that history. No results are sent to a server.

Only successful attempts are saved persistently. An unfinished attempt is lost when the page is reloaded. Clearing site data removes saved history, and private browsing or browser settings may prevent persistent storage. Storage behavior for locally opened files can vary between browsers. Download JSON files to keep a separate copy or share results. JSON import is not currently supported.

## Publish with GitHub Pages

Place `index.html` and this `README.md` at the root of a GitHub repository. In the repository settings, enable Pages, choose **Deploy from a branch**, and select the branch containing these files and the **/(root)** folder.

The simulator is a static site and requires no backend or external dependencies. Once published, visitors can use it directly in their browsers.

