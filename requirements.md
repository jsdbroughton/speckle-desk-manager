## Requirements

A web fronted application to:

- present the current arrangement of people, projects and desks.
- offer a means for developing options and offering them for comment.

### Future

- offer automated layout options

## Entities

### Physical Entities:

- `Desk`
- `Building`
- `Floor`
- `Person`
- `Equipment Sets`

### Intangible Entities:

- `Project`
- Person `Role`s
  - `Manager`
  - `Architect`
  - `Support`

## Planning Goals

- `Project` teams to sit contiguously
- `Manager`s' teams should be approximately adjacent
- `Support` are evenly distrubuted to `Floor`s
- `Support` are adjacent to `Manager`s

## Model Constraints (May be conflicting)

- Projects with >= 10 Staff require 10% free desks
- Relationships:
  - `Building 1-∈ Floor⋲⋺`
  - `Desk ⋺-1 Floor`
  - `Desk 1-1 Person`
  - `Architect ⋺-1 Project`
  - `Architect ⋺-1 Manager`
  - `Manager 1-⋲ Project`
  - `Manager 0/1-1 Support`
  - `Person 1-1 Role`
  - `Equipment Set 1-1 Desk`
