# GravityCheck — Structural Integrity for Satisfactory

GravityCheck adds realistic structural integrity to your factory. Buildings need proper support or they'll come crashing down!

## How It Works
- **Foundations** have a maximum overhang of **4 tiles** from a grounded support point
- **Walls and pillars** act as **load-bearing structures** — building a pillar under your platform resets the overhang counter
- Unsupported foundations glow **yellow** (at the limit) or **red** (unsafe) as a warning
- After **3 seconds** without support, unsafe foundations are **auto-demolished** with physics
- **Everything on top** (machines, conveyors, etc.) **collapses with the foundation** — falling with full gravity simulation

## Features
- 🔴 Visual glow warnings (yellow = at limit, red = unsafe)
- 🧱 Walls & pillars provide structural support
- ⏱️ 3-second repair window to fix unsafe structures
- 💥 Physics-based destruction — buildings fall realistically
- 🔗 Cascade demolition — machines on collapsed foundations fall too
- ⌨️ Press **G** to toggle highlight overlay on/off

## Tips
- Use **pillars** to extend your factory over gaps and cliffs
- Place **walls** under elevated platforms for support
- Watch for **yellow glow** — it means you're at the edge of stability
- You have **3 seconds** to add support before an unsafe structure collapses

## Technical
- Uses BFS-based distance calculation from grounded supports
- Load-bearing elements (walls/pillars) reset distance within 500cm vertical and horizontal range
- Polling-based structural change detection (1s interval)
- Compatible with the lightweight buildable system
