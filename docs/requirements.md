# Requirements

## 1. Project Scope

### R-001 — Main Experience

Classic Pong must provide a classic Pong experience that is playable and stable.

### R-002 — Main Game Mode

Version 1.0 must include **Player vs CPU** matches.

### R-003 — Local Multiplayer

Local multiplayer is outside the scope of version 1.0 and is planned for version 2.0.

### R-004 — Online Multiplayer

Online multiplayer is outside the scope of the project.

### R-005 — Future Expansions

Mechanics and modes planned for a future expansion or project, such as Pong Sports, are not part of Classic Pong 1.0.

---

## 2. Player

### R-006 — Movement

The player must be able to move only along the axis related to the game orientation.

### R-007 — Movement Speed

The player's movement speed must be configurable.

### R-008 — Keyboard Support

The game must support keyboard input.

### R-009 — Controller Support

The game must support gamepads/controllers.

### R-010 — Control Configuration

Player controls must be configurable.

### R-011 — Side Selection

The player must be able to select their side before starting a match.

### R-012 — Side Changes During a Match

The player must not be able to change sides during an active match.

---

## 3. CPU

### R-013 — CPU Opponent

The game must include a CPU opponent in version 1.0.

### R-014 — CPU Movement

The CPU must use the same movement speed configured for the player.

### R-015 — Difficulty

The game must provide multiple CPU difficulty levels.

### R-016 — Detection

Difficulty must affect the range in which the CPU can detect the ball.

### R-017 — Reaction Time

Difficulty must affect the CPU's reaction time.

### R-018 — Prediction

Higher difficulty levels must allow the CPU to progressively move from reacting to the ball to predicting its path and calculating where to intercept it.

### R-019 — CPU Errors

The CPU must be able to make mistakes and miss the ball.

### R-020 — CPU Configuration

The player must select a difficulty level, but must not directly configure the CPU's internal behavior parameters.

---

## 4. Ball

### R-021 — Movement

The ball must move continuously while it is active.

### R-022 — Minimum Speed

The ball must not stop during active gameplay.

### R-023 — Initial Speed

The initial ball speed must be configurable before starting a match.

### R-024 — Speed Changes

The ball speed must be able to increase or decrease during a match.

### R-025 — Maximum Speed

There must not be a separate setting for maximum speed. The maximum speed must remain proportional to the configured ball speed.

### R-026 — Bounce

The ball's bounce direction must depend on the point where it hits the paddle.

### R-027 — Bounce Configuration

The bounce behavior must not be configurable by the player.

### R-028 — Serve Direction

The initial serve direction must be selectable before starting the play.

---

## 5. Playfield and Boundaries

### R-029 — Boundaries

The playfield must have physical boundaries that allow the ball to bounce.

### R-030 — Goals

The playfield must have goal areas at the ends assigned to each player.

### R-031 — Orientation

The match must allow the player to select horizontal or vertical orientation.

### R-032 — Horizontal Orientation

In horizontal orientation, the players must be placed on the left and right sides of the playfield.

### R-033 — Vertical Orientation

In vertical orientation, the players must be placed at the top and bottom of the playfield.

---

## 6. Goals and Score

### R-034 — Goal

When the ball passes through a player's goal, the opponent must receive one point.

### R-035 — End of Play

After a goal, the current play must stop.

### R-036 — Ball Out of Play

After a goal, the ball must be out of play until the next serve.

### R-037 — Reset

After a goal, the player who received the goal must be able to reset the ball to the center.

### R-038 — Serve After a Goal

The player who received the goal must start the next play using a serve action.

### R-039 — Waiting for Serve

The game must remain stopped after a goal until the serve action is performed.

### R-040 — Repeat

The game cycle must be able to repeat after every goal.

---

## 7. Game Modes

### R-041 — Points Mode

The game must support matches based on a number of points.

### R-042 — Points Target

The number of points required to finish a match must be configurable.

### R-043 — Time Mode

The game must support matches based on a time limit.

### R-044 — Match Duration

The duration of a time-based match must be configurable.

### R-045 — Match Point

The game must support a Match Point-based game mode.

### R-046 — Combined Conditions

The system must allow matches to use the available end conditions when required.

### R-047 — Sudden Death

A "next goal wins" mode is not part of Classic Pong 1.0.

### R-048 — Future Sudden Death

A "next goal wins" mode may be added as part of local multiplayer in version 2.0.

---

## 8. Match Configuration

### R-049 — Match Setup

The player must be able to configure the match before starting it.

### R-050 — Match Parameters

The configuration must include, at minimum:

* Game mode.
* Points target, when applicable.
* Match duration, when applicable.
* CPU difficulty.
* Player movement speed.
* Initial ball speed.
* Orientation.
* Player side.
* Serve direction.

### R-051 — Later Changes

The configuration of a new match must be changeable after a match ends.

---

## 9. Match Flow

### R-052 — Start

The game must allow the player to start a match from the match configuration screen.

### R-053 — Start of Play

The play must start with a serve.

### R-054 — Main Game Loop

The main game loop must include:

**Serve → movement → bounces → goal → score → reset → new serve.**

### R-055 — End of Match

The match must end when the configured win condition is reached.

### R-056 — Result

The result must be shown when a match ends.

### R-057 — Rematch

The player must be able to start a rematch using the corresponding configuration.

### R-058 — Rematch with Side Change

The player must be able to start a rematch with the player sides changed.

### R-059 — New Match

The player must be able to return to match configuration and start a new match with different settings.

---

## 10. HUD

### R-060 — Score

The HUD must always show both players' scores during the match.

### R-061 — Serve Indicator

The HUD must show who must serve when the match is waiting for a player action.

### R-062 — Timer

The HUD must show the remaining time when using Time Mode.

### R-063 — Game Mode

The HUD must allow the player to identify the active game mode.

### R-064 — Match Point

The HUD must show the Match Point status when applicable.

### R-065 — Pause Status

The pause state must be visible when the match is paused.

### R-066 — HUD Customization

The player must be able to change the HUD position, size and colors.

### R-067 — Presets

The HUD must support predefined configurations.

---

## 11. Menus

### R-068 — Main Menu

The main menu must include, at minimum:

* Play.
* Options/Settings.
* Exit.

### R-069 — Match Configuration

Match configuration must be inside Play and must not be a separate main menu option.

### R-070 — Pause

The match must be pausable.

### R-071 — Pause Options

The pause menu must allow the player to:

* Continue.
* Restart the match.
* Return to the main menu.

### R-072 — Pause Behavior

When the match is paused, the timer and game simulation must stop.

### R-073 — Settings Access

General settings must be accessible from the main menu and during the pause.

### R-074 — Match Result

The match result must have its own screen/menu.

### R-075 — Result Options

The result menu must allow the player to:

* Rematch.
* Rematch with changed sides.
* Configure a new match.
* Open options/settings.
* Return to the main menu.

### R-076 — Victory and Defeat

In matches against the CPU, the result must distinguish between victory and defeat.

### R-077 — Multiplayer

Future multiplayer matches do not need a victory/defeat presentation focused on the CPU.

---

## 12. Audio

### R-078 — Music

Classic Pong must not include music as a requirement for version 1.0.

### R-079 — Interface Sound

The game must have a separate volume setting for interface sounds.

### R-080 — Game Effects

The game must have a separate volume setting for gameplay sound effects.

### R-081 — Gameplay Effects

The game must include sound effects for relevant events, including:

* Ball/paddle.
* Ball/boundary.
* Serve.
* Goal.
* Point.
* Victory against the CPU.

### R-082 — Interface

The game must include sounds for relevant interface interactions.

---

## 13. Visual Presentation

### R-083 — Style

The game must use an original minimalist/arcade visual style.

### R-084 — Original Assets

The main visual elements must be created specifically for the project.

### R-085 — External Assets

Downloaded third-party visual assets must not be used as the base of the visual style.

### R-086 — Visual Identification

The player, CPU and ball must be visually distinguishable.

### R-087 — Colors

The colors used by the main elements must be configurable.

### R-088 — Visual Effects

Advanced visual effects, such as particles, screen shake or complex impact effects, are not requirements for the initial version and may be added later.

---

## 14. Display and Window

### R-089 — Display Mode

The game must allow the player to configure the display mode.

### R-090 — Window Mode

The game must support both windowed and fullscreen modes.

### R-091 — Window Resizing

The presentation must adapt to window resizing.

### R-092 — Resolution

The game must support resolution configuration.

### R-093 — Scalability

The game must keep a functional presentation at different resolutions without requiring high-end hardware.

---

## 15. Persistent Settings

### R-094 — Saving Settings

The game must save the general and match settings selected by the player.

### R-095 — Loading Settings

When the game starts again, the saved settings must be available.

---

## 16. Stability Requirements

### R-096 — Playability

Version 1.0 must allow complete matches from start to finish.

### R-097 — Stability

Version 1.0 must run stably during normal matches.

### R-098 — Complete Flow

The player must be able to complete the full flow:

**Main menu → configuration → match → result → rematch/new match/main menu.**

### R-099 — Distribution

Version 1.0 must be available as a playable build that can be tested by other people.

---

## 17. Out of Scope for Classic Pong 1.0

The following elements are not part of the requirements for version 1.0:

* Local multiplayer.
* Online multiplayer.
* "Next goal wins" mode.
* Pong Sports mechanics.
* Dash.
* Direct configuration of individual CPU behavior parameters.
* Independent bounce behavior configuration.
* Music.
* Advanced visual effects.

These elements may be evaluated for future versions, but they are not part of the committed scope of Classic Pong 1.0.
