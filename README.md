## Data Guide

Each market folder contains a station and ads file. The ads file contains foreign keys to both the station and PAC files.

At the top level, the PAC file will span all DMA's in a state. Airtime is currently WIP, is only available for ads scraped from invoices.
## Variable Definitions

### Station

| Column  | Status                            |
|---------|-----------------------------------|
| Sign    | Station call sign, in format K... |
| Network | All major networks                |
| Medium  | Only broadcast currently          |
| DMA     | Only Phoenix currently            |
| State   | Only AZ currently                 |
| Channel | Channel number                    |

### PAC

| Column   | Status                                                    |
|----------|-----------------------------------------------------------|
| Name     | PAC Name                                                  |
| Juris    | Whether an IE committee or candidate.                     |
| Side     | What side of a race a PAC spent on. Ex: Dem, Rep, Yes, No |
| Cycle    | 2018 only                                                 |
| District | U.S. House district if applicable                         |

### Ads

| Column    | Status                                    |
|-----------|-------------------------------------------|
| Stationid | Foreign key to Stations                   |
| Pacid     | Foreign key to Pacs                       |
| Airdate   | ISO8601 date of ad airing                 |
| Cycle     | Cycle ad airs                             |
| Rate      | Float specifying price of individual spot |
| Program   | The program title the ad aired on         |
| Airtime   | WIP, time ad aired.                       |