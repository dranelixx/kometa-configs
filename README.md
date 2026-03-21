# Kometa Collection Configs

Custom [Kometa](https://kometa.wiki/) collection configurations for Plex media libraries.

## Structure

```
movies/
├── charts.yml        # Plex Popular, Trending, Top Rated, Best of Year
├── genres.yml        # IMDb genre collections (Action, Comedy, Horror, etc.)
├── studios.yml       # DC Extended Universe, Marvel Studios
├── specials.yml      # Mindfuck, Time Travel, Outer Space, Superhero
├── movies.yml        # Custom collections (Cloverfield, Stand Up, Pokémon, etc.)
├── collections.yml   # TMDB collection definitions (Indiana Jones, James Bond, etc.)
└── merges.yml        # Multi-TMDB-collection merges (Alien, X-Men, Middle Earth, etc.)

shows/
├── charts.yml        # Plex Popular, Trending, Top Rated, Emmy Winners
└── shows.yml         # Custom show collections
```

## Usage

Referenced in `kometa.yml` via `git:`:

```yaml
libraries:
  Movies:
    collection_files:
      - git: dranelixx/kometa-configs/movies/charts
      - git: dranelixx/kometa-configs/movies/genres
      - git: dranelixx/kometa-configs/movies/collections
      # ...
  Shows:
    collection_files:
      - git: dranelixx/kometa-configs/shows/charts
      # ...
```

Changes on `main` are picked up automatically on the next Kometa run.
