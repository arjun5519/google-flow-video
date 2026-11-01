---
name: google-flow-video
description: Turn a topic into a researched Google Flow video package with timed clips, generated start and end frame images, narration, and ready-to-paste motion prompts. Use for educational, explanatory, or promotional video preparation for Google Flow.
---

# Google Flow video preparation

Deliver a complete video preparation package when the user supplies a topic. An example topic is an EV car battery pack; do not assume that topic for other requests. This workflow prepares assets and scripts. Operate Flow or generate paid video clips only when the user requests that additional work.

## Establish the brief

Use the user's topic, uploaded images, duration, language, audience, visual style, and aspect ratio. Ask only about missing information that materially blocks the work. Otherwise state practical assumptions and proceed: accessible educational narration in the user's language, landscape 16:9, and a coherent realistic visual style. Estimate duration from the subject's essential teaching points and natural narration pace when none is supplied; explain the estimate briefly.

## Research facts and visual references

Search the web for the topic and relevant images. Prefer primary technical sources, manufacturers, research papers, and official documentation. Separate verified facts from illustrative simplifications. For an EV pack, distinguish chemistry-dependent and manufacturer-dependent designs; avoid presenting one pack architecture as universal.

Inspect candidate reference images before choosing them. Prioritize suitable user uploads, then relevant internet images with clear provenance and usable rights, or generate an original illustration when existing images are unsuitable. Record source-page links, attribution, and known usage restrictions for selected internet assets; never assume that search visibility grants reuse rights. References and generated illustrations must be labeled distinctly. Never describe an AI illustration as documentary evidence.

## Plan timing for the selected Flow model

Verify current clip lengths, aspect ratios, and first/last-frame support using official Google Flow documentation and, when available, the user's selected model settings:
- https://support.google.com/flow/answer/16352836
- https://support.google.com/flow/answer/16353334

Capabilities vary by model and may change. Do not assume every model supports ten-second clips or both boundary frames. Use clips of ten seconds or less supported by the selected model. If the model is unknown, identify that uncertainty and choose a documented compatible option, clearly naming the assumption.

Respect the user's requested final runtime. Create a table with clip number, timeline in/out, final duration, generation duration, and teaching point. Sum final clip durations and check for gaps or overlaps. If the runtime is not a multiple of supported generation lengths, generate a supported length and specify the trim needed. Account for overlap when using dissolves. Keep one clear visual action per short clip.

Write narration that fits: estimate speech at roughly 130–150 words per minute with room for pauses, and revise to match the audience and language. Distinguish estimated speech time from measured time; never claim a recording was timed unless it was.

## Create actual boundary images

For every clip deliver a usable starting-frame image and ending-frame image, plus the exact prompts used. Image prompts alone do not fulfill this step. Use the available image-generation/editing tool and follow its applicable skill. Inspect uploaded/local references before editing. When tools or required reference files are unavailable, explicitly identify the missing assets and deliver the rest without claiming completion.

Define a shared visual guide before generation: subject geometry, component arrangement, colors, materials, lighting, aspect ratio, environment, and camera conventions. Use reference-based edits to preserve identity across frames. For a continuous shot, reuse the exact previous ending-frame file as the next starting-frame file. A deliberate cut may use a different composition while retaining subject identity.

Design start and end frames that can be connected by plausible motion within the clip. Avoid impossible camera moves, abrupt topology changes, and inconsistent component counts. For technical cutaways, maintain factual geometry and mark simplified diagrams as illustrative. Put precise labels and captions in the editing plan rather than relying on generated image text.

Inspect generated frames for continuity, technical plausibility, framing, and unwanted text. Correct visible defects before delivery. Name each frame by clip number, timeline, and role using the default pattern `clip-01_00-00_to_00-10_start.png` and `clip-01_00-00_to_00-10_end.png` (minutes-seconds, zero padded). Derive these names from the final timeline after timing is fixed; use the exact same names in the script, asset links, and delivery checklist. If a boundary image is reused, copy the identical image under the next clip's start filename so each Flow input slot has an obvious matching file. If the timeline changes, rename affected files and update all references before delivery.

Save every selected or generated frame as an actual downloadable PNG in the user-facing output folder. A chat preview or a web URL alone does not fulfill delivery. If an internet image is selected, save the permitted source locally and make a PNG copy for the Flow package while retaining its source-page link and attribution; if download or reuse is not permitted, choose another image or generate an original one. Check each delivered file's PNG signature and openability. Keep the final PNGs together and create a ZIP containing all of them, with filenames matching the script. Link the ZIP and direct PNG files in the final chat response, and embed each start and end image inline beside its clip script. If the same image is reused, explain that the ZIP may contain two named copies for the two Flow input slots.

## Write a separate script for each clip

For each numbered clip provide:
1. Timeline and generation length, including any trim.
2. Purpose and visible action.
3. Embed the actual starting and ending images directly in the script section using Markdown image syntax, with captions `Start frame` and `End frame`. Show the exact filename next to each caption so it can be matched to the file in Flow. Use relative image paths in a saved Markdown script when images are in the same folder, and absolute paths in the chat response. Repeat the identical filenames in Flow input instructions. Do not make the user open links merely to see the frames.
4. Starting-frame and ending-frame image prompts.
5. A paste-ready Flow prompt describing the subject, action between frames, camera movement, lighting, visual continuity, and relevant constraints. Keep instructions achievable within the clip length.
6. Exact narration/dialogue, estimated spoken duration, and intentional pauses.
7. On-screen text, sound/music cues, and transition/editing notes.

Separate voiceover text from visual generation instructions so it is clear whether narration will be added during editing or requested as native generated speech. Do not promise exact generated speech or sound synchronization.

## Deliver and check

Provide a short concept and assumptions, research notes with source links, the full timeline, the visual guide, and all numbered clip packages. Save user-facing frame assets and a reusable script document in the workspace's designated output folder. Link the files in the final response.

Check that every clip has both frame assets, a motion prompt, narration or an explicit silence cue, and timing. Verify total final runtime, consistent numbering, accessible asset links, and source attribution. Report any ungenerated or unavailable assets precisely. Do not claim the final video exists when only the preparation package has been created.

