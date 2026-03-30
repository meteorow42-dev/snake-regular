# Snake

Classic Snake implemented as a tiny static app with no external dependencies.

## Run

1. Fastest option on Windows: double-click `Snake.exe`.

   It starts the local server and opens the game in your default browser.
   Keep the launcher window open while you play.

2. Fallback: start the local server manually:

   ```powershell
   powershell -ExecutionPolicy Bypass -File .\scripts\dev.ps1
   ```

3. Open `http://localhost:4173`.

You can also open `index.html` directly in a browser if you only need a quick preview.

## Manual checklist

- Start the game with the Start button or any movement key.
- Move with Arrow keys, `WASD`, or &#1062;&#1060;&#1067;&#1042;.
- Check that quick back-to-back turns still feel responsive.
- Check that food increases the score and grows the snake.
- Pause and resume with Space or the Start button.
- Restart with the Restart button or `R`.
- Verify that hitting a wall or the snake body ends the run.

## Notes

- The workspace was empty and had no existing framework or test runner, so this stays as a plain browser app.
- The game rules are isolated in `src/snake-logic.js` for deterministic behavior and easy future testing.
- Rendering now uses `requestAnimationFrame` for smoother visuals while the game step still runs on the same classic tick.
- `Snake.exe` is built from `scripts/SnakeLauncher.cs` and can be rebuilt with `powershell -ExecutionPolicy Bypass -File .\scripts\build-launcher.ps1`.
