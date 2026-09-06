# Blockshot

**The image and video board.** One line about a story becomes a cast, the sets, a shot list and one
picture per shot — drawn on your own PC by your own ComfyUI, written by a local text model. Nothing
leaves your machine. No credits, no cloud.

With **Pro** on, every shot becomes a short video, the eyes check every picture and take and redraw the
misses, and one button runs the whole thing overnight and cuts the film. Pro switches on with the
Blockshot key from your Stable Yogi account page — one setup file for everyone.

> **Early test (0.2.1).** This is the first public build. Please break it and tell me:
> your Stable Yogi account page (Settings → API, the Blockshot card) · the Discord · or open an issue here.

## Download

Get the setup file from the **Releases** page on the right. Two files:

| File | What it is |
|---|---|
| `Blockshot-Setup-0.2.1.exe` | installs per user into `%LOCALAPPDATA%\Blockshot`, no admin, touches nothing else |
| `Blockshot-0.2.1-portable.zip` | unzip anywhere, double-click `Blockshot.cmd` |

Each file has a `.sha256` next to it. The setup is not code-signed, so Windows shows its SmartScreen
box once: **More info → Run anyway.**

## The first film, and the example inside

"Marry Me, Maybe" (75 s) was written, drawn, rolled and cut inside Blockshot from one line of idea and twelve
lines of script. The same board ships inside the app: click **Open the example board** and look at every part,
film included. How it was made, step by step: the lessons on the portal (the **Lessons** button in the app).

Every picture and video the app makes is written without the maker's data: no prompt, no model names, no seeds
inside a file you share.

## What you need on the PC

- Windows 10 or 11, an NVIDIA card with 12 GB or more.
- **ComfyUI** (the Painter) — any install: portable, desktop, Stability Matrix. Blockshot finds it.
- **A writing model** (the Writer) — inside LM Studio, or any OpenAI-style server. Download it from
  LM Studio's own search page (2 to 9 GB, an 8B model is plenty), then switch LM Studio's server on.
- The model pack for the starter workflow: the Muse by Stable Yogi checkpoint (free on Civitai or
  from the portal), plus its text encoder and VAE (the app downloads those two). Already have the files?
  Point the app at that folder — nothing downloads twice.

> **The two model kinds are not interchangeable.** Your ComfyUI `.safetensors` draw; they cannot write.
> The Writer's model is a separate download inside LM Studio, even when your ComfyUI folder is full.
> Point LM Studio at a ComfyUI folder and it answers `No LM Runtime found for model format
> 'torchSafetensors'`. Five-minute walk-through: <https://forgebun.com/go/bs_writer>

## What Free does

- Idea → Write → Draw → a storyboard: outline, cast sheets, set references, one frame per shot.
- Unlimited boards, unlimited pictures, forever. Your own models: import any ComfyUI workflow with the
  Blockshot tags and it becomes a step.
- Script in, board out: paste a script and the Writer follows it word for word.
- Four of each: four seeds per frame, keep the one you like.
- Sheet and Export: the storyboard on one printable page, a shot list CSV, a folder that travels.
- Reuse people: the same faces in the next episode.

## What Pro adds

- **Takes:** one video per shot from its kept frame.
- **The eyes:** a vision model scores every picture and take and redraws the misses.
- **Cut:** the takes joined into one film.
- **Overnight:** one button, wake up to a film.
- **Hand it to Claude:** an MCP server so Claude Code, Claude Desktop or a local model runs the board for
  you (`claude mcp add blockshot -- "%LOCALAPPDATA%\Blockshot\python\python.exe" -m blockshot.agent.mcp`).
- The Muse Pro model and the Video pack links.

Pro is a Stable Yogi membership: paste your Blockshot key (account page → Settings → API → Blockshot) under Settings → Licence. One key, one PC at a time —
move it when you need.

## First run

1. Start ComfyUI and your text model server.
2. Run Blockshot. The wizard finds both, gets the model pack, checks the starter workflow and draws one
   test picture.
3. New board → type an idea → Write → Draw. Open the viewer on any picture, Redo or Keep.

The engine is a plain local API, documented live at `http://127.0.0.1:7150/v1/docs`.

## Learn it

- Six short lessons, in the order you use the app: https://forgebun.com/go/bs_learn
- How the first film was made, and what went wrong: https://forgebun.com/go/bs_film

## Feedback

Tell me what broke, what confused you, and what you want next. Early-test feedback shapes 0.3.
