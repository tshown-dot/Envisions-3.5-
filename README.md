# Variable Vault 🔐

A heist game for **enVision 2.0 · Grade 6 · Topic 3 · Lesson 3-5: Evaluate Algebraic Expressions**.

Students substitute values into variables by dragging "intel cards" onto the variables in a lock expression. Then they evaluate using the order of operations to crack the code.

- 5 vaults × 3 locks, about 10 minutes
  1. **Lobby Lockbox:** one variable (`4x + 7`)
  2. **Twin-Key Treasury:** two or three variables (`3a + 2b`, `5(x + y)`, `xy − 4`)
  3. **Power Core:** exponents and order of operations (`n² − 3n`, `2(y − 1)²`)
  4. **Fraction & Decimal Den:** decimal and fraction values
  5. **Grand Vault:** formulas in word problems (`P = 2ℓ + 2w`, `A = ½bh`, `d = rt`, `V = s³`)
- Problems are randomly generated, so every play-through is different.
- Wrong answers set off an alarm and give a targeted hint. The game detects common mistakes:
  - reading `3x` as "3_" (a two-digit number)
  - treating `n²` as `n × 2`
  - working left to right instead of following the order of operations
- Two misses trigger a **lockdown**: the game shows the full step-by-step solution, then gives the student a backup lock of the same type.
- The end-of-game **Heist Report** shows loot, accuracy, first-try stars, time, and "skills to sharpen."
- It works with a Chromebook trackpad, a touchscreen, or a keyboard. Students can type answers or use the on-screen keypad.

It's a single `index.html` file with no build step, no external libraries, and no outside fonts, so it loads on locked-down school networks.

## Deploy on Render (from GitHub)

1. Create a new GitHub repo, for example `variable-vault`, and upload `index.html`, `render.yaml`, and this README.
2. In Render, choose **New → Static Site** and connect the repo.
3. Use these settings:
   - **Build command:** *(leave blank)*
   - **Publish directory:** `.`
4. Click **Create Static Site**. Render gives you a URL like `https://variable-vault.onrender.com` to post in Google Classroom.

You can also use **New → Blueprint** in Render, which reads the included `render.yaml`.

Every push to GitHub redeploys the site automatically.

## Teacher tips

- **Starting vault:** students can start at any vault from the title screen. This is useful for differentiation or for picking up where they left off.
- **Proof of play:** have students screenshot the Heist Report (Chromebook: `Ctrl + Shift + Show windows`), or turn it in on Google Classroom.
- **Best score:** the best score is saved in each student's browser on that device.

## Future upgrades (database-ready)

The game state lives in one object (`window.__vv` in the browser console). A class leaderboard or teacher dashboard can be added later with a small Render Web Service and a Render Postgres database, with the Heist Report sending results to it.
