# Basic Species Traits

## Biological uniqueness
Each and every species should have some unique modifier values based on biological origin. The modifiers for all species are:
  * Leader age
  * Pop growth speed
  * Environment tolerance

Base leader age to be adjusted based on the following ratio:
  * min = leader_age / 6
  * max = leader_age * 5 / 6

The cap for biological modifiers is calculated based on the following formula:
  * 0.05 * leader_age + 0.8 * pop_growth_speed + 0.15 env_tolerance

The cap should be around **0.15** with a very little deviation

## Social uniqueness
Every species should have some unique social modifiers based on it's origin and evolution. Basically, there should be two buffs and one debuff.

The modifiers should be splitted into two categories:
  * Living standard (amenities, housing, happiness, etc.)
  * Job related stuff (productivity, upkeep, etc.)

Basically there should be buff and debuff for living modifiers and only buff for job related stuff

The cap for social modifiers is calculated based on the following formula. Do not forget about the contexto - some modifiers may have negative values which we need to consider as positive and vice versa (e.g. housing):
  * (0.35 * Σ living_mods) + (0.65 * Σ job_mods)

The cap should be around **0.15** with a very little deviation

## Habitability
Each and every species should have a primary planet type, secondary, tertiary, rare and restricted habitability. This rule does not apply for robots & machines - they can live anywhere. The hierarchy should be based on the climate - the same climate type should fall under the secondary group. Tertiary and rare are other two groups and those two which are left are under restricted tag.

As an example, reptiloids may have the following hierarchy:
### Primary
  * Desert - 100%
### Secondary
  * Arid - 75%
  * Savannah - 75%
### Tertiary
  * Continental - 50%
  * Ocean - 50%
  * Tropical - 50%
### Rare
  * Alpine - 25%
  * Tundra - 25%
  * Arctic - 25%
### Restricted
  * Volcano - -200%
  * Tomb - -200%
  * High pressure - -200%
  * Plasma - -200%