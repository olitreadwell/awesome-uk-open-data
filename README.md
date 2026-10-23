# Awesome UK Data [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of UK data sources, APIs, registers and portals, tagged with what each one is and what it takes to use it.

The list is also published as a searchable site at <https://olitreadwell.github.io/awesome-uk-open-data/>, generated from this README by `scripts/build_site.py`.

## Contents

- [Legend](#legend)
- [Start here](#start-here)
- [Central government and agencies](#central-government-and-agencies)
- [Statistics and economics](#statistics-and-economics)
- [Health and social care](#health-and-social-care)
- [Environment, climate and geospatial](#environment-climate-and-geospatial)
- [Transport](#transport)
- [Energy and utilities](#energy-and-utilities)
- [Education and research](#education-and-research)
- [Devolved administrations](#devolved-administrations)
- [Local and regional data](#local-and-regional-data)

## Legend

Every entry is tagged with what it is, what it takes to use, and whether it is still the current tool for that data.

Each tag has its own shape, so the tags can be told apart without relying on colour. On the site the colour marks which axis a tag belongs to: blue for type, green for access, amber for status.

- Type: `⇄ API` (a programmatic interface), `▦ Data` (datasets you download or query), `☰ Portal` (a site you search across many datasets), `☑ Register` (an official register you look records up in), `¶ Docs` (documentation or metadata with no data of its own).
- Access: `○ Open` (no key and no account needed), `◑ Key` (API key or developer registration), `◕ Login` (user account), `● Paid`. The shape fills up as the access gets harder: empty is open, solid is paid.
- Status: `⟳ Legacy` (still online, but superseded) or `▣ Archived` (frozen snapshot). No status tag means current.

Tags sit between the link and the description, in that order:

```
- [Name](https://example.gov.uk/) - ▦ Data - ○ Open - what it holds.
- [Name](https://example.gov.uk/) - ⇄ API - ◑ Key - ⟳ Legacy - what it holds.
```

Dead links are repaired or dropped as they are found, and a weekly job re-checks every link.

## Start here

These cover most requests. Each one is listed in full under its publisher below.

- Data.gov.uk - the catalogue of UK government datasets
- Office for National Statistics - official statistics, the ONS API and the geography portal
- OS Data Hub - Ordnance Survey maps, addresses and places
- Companies House API - the company register as JSON
- TfL Unified API - live London transport data
- Environment Agency - flood warnings, river levels and water quality
- NHS England - hospital, workforce and GP practice data
- The Gazette - the official public record, as linked data

## Central government and agencies

- [GOV.UK](https://www.gov.uk/) - ☰ Portal - ○ Open - The UK government site: content API, search, and the GOV.UK Design System, publishing government information as open data.
- [Data.gov.uk](https://www.data.gov.uk/) - ☰ Portal - ○ Open - UK open data catalog: 10,000+ datasets from UK government departments and public bodies, with a CKAN API and DCAT metadata.
- [legislation.gov.uk](https://www.legislation.gov.uk/) - ☑ Register - ○ Open - The official statute book of the UK, available as structured XHTML, XML, and RDF for reuse, with a search API.
- UK Parliament
    - [UK Parliament API](https://api.parliament.uk/) - ⇄ API - ○ Open - Parliamentary data APIs: bills, MPs, members’ interests, petitions, and Hansard content in structured JSON.
    - [UK Parliament Members API](https://members-api.parliament.uk/) - ⇄ API - ○ Open - The UK Parliament Members API lists MPs and peers with their party, house, and dates of service, and reports the state of the parties in each house. The state-of-the-parties call takes a house, 1 for the Commons and 2 for the Lords, and a date, and returns each party with the seats it holds and the members counted behind them: on 1 October 2026 the Commons held 650 seats across 18 parties, with Labour on 403 and the Conservatives on 118. It answers without a key and sits alongside the main Parliament APIs on api.parliament.uk, and Parliament publishes the data under the Open Parliament Licence v3.0.
- [The National Archives Discovery API](https://discovery.nationalarchives.gov.uk/) - ⇄ API - ○ Open - REST API over Discovery, the catalogue of records held by The National Archives and archives across the UK: search records, archive collections and file authorities, and fetch record details, hierarchies and reference data.
- [Planning Data](https://www.planning.data.gov.uk/) - ⇄ API - ○ Open - Ministry of Housing, Communities and Local Government platform for planning and housing data in England. One API serves over 100 datasets, from conservation areas and listed buildings to brownfield land and flood risk, and every dataset can be downloaded in bulk.
- [Find a Tender Service](https://www.find-tender.service.gov.uk/) - ⇄ API - ○ Open - Find a Tender is where UK public sector buyers publish notices about procurement opportunities and contracts, run by the Cabinet Office. Notices from February 2025 follow the Procurement Act 2023 and cover the full contract life cycle outside Scotland, while earlier procurements stay in the notice search. The same notices appear as Open Contracting Data Standard release packages over a JSON API that answered a plain request with records updated on 29 September 2026, and Find a Tender took over from Tenders Electronic Daily in the UK on 31 December 2020.
- [GOV.UK Trade Tariff API](https://www.gov.uk/trade-tariff) - ⇄ API - ◑ Key - The GOV.UK Trade Tariff API is HMRC's JSON interface to the UK Trade Tariff, covering commodity codes, duties and VAT rates, quota measures and historical tariff data. It is updated daily, with documentation at docs.trade-tariff.service.gov.uk and an entry in the government API catalogue that places the data under the Open Government Licence v3.0. The sections endpoint returned 21 sections on 29 September 2026, and the heading and commodity endpoints return the goods nomenclature records behind a code. The newer service on api.trade-tariff.service.gov.uk issues OAuth credentials through HMRC's developer portal, and rate limiting came in from September 2026.
- [The Gazette](https://www.thegazette.co.uk/data) - ☑ Register - ○ Open - The Gazette is the official public record of the UK, published since 1665 and produced by TSO under the superintendence of HM Stationery Office, part of The National Archives. Its archive holds company, insolvency, wills and probate, planning, honours and appointment notices, and it publishes them as linked data: a linked data API returns each notice as JSON-LD, Turtle or RDFa-enriched XML from format-specific URLs, and an Atom feed carries the latest notices and accepts search parameters such as text and start-publish-date. The site states the content is Crown copyright and free to use under the Open Government Licence v3.0, with the licence not covering the re-use of personal data.
- [Charity Commission Register of Charities](https://register-of-charities.charitycommission.gov.uk/) - ☑ Register - ○ Open - The Charity Commission register for England and Wales as a daily extract, published as JSON and tab-delimited files: charity records plus trustee, annual return, classification, area of operation and governing document tables.
- [Companies House API](https://developer.company-information.service.gov.uk/) - ⇄ API - ◑ Key - Free JSON APIs for the UK company register: company profiles, officers, filings, and disqualified directors with an API key.
- [HM Land Registry Data](https://landregistry.data.gov.uk/) - ▦ Data - ○ Open - Price paid data, property alerts, and INSPIRE spatial datasets for England and Wales, free under open licenses.
- [UK Police Data](https://data.police.uk/) - ⇄ API - ○ Open - Street-level recorded crime, stop and search, and outcomes data for all forces, updated monthly.
- [DWP Stat-Xplore](https://stat-xplore.dwp.gov.uk/) - ☰ Portal - ○ Open - The Department for Work and Pensions' tool for benefit statistics: choose a dataset, build a custom table, view it as a chart and download the result in common file formats. Guest access is free, and a free account adds saved tables, field customisation and queued large tables. Information in Stat-Xplore sits under the Open Government Licence, and the REST API under /webapi/rest/v1/ needs an account.

## Statistics and economics

- Office for National Statistics
    - [Office for National Statistics](https://www.ons.gov.uk/) - ☰ Portal - ○ Open - ONS: official UK statistics on population, economy, labour market, and society, plus the ONS API (api.ons.gov.uk) and data explorer.
    - [ONS Open Geography Portal](https://geoportal.statistics.gov.uk/) - ▦ Data - ○ Open - Boundary data and geographies for UK statistics: output areas, wards, local authorities, and census geographies as downloads and APIs.
- [Nomis](https://www.nomisweb.co.uk/) - ☰ Portal - ○ Open - Nomis is the official census and labour market statistics service, run by the University of Durham on behalf of the Office for National Statistics and first launched in 1981. It holds employment, unemployment, earnings and population figures by geography, sex, age and industry, drawn from the Labour Force Survey, the Annual Survey of Hours and Earnings, the Claimant Count, the Business Register and Employment Survey and the census. The REST API (v01) covers dataset discovery and data downloads in SDMX XML or JSON, CSV and JSON, with a query builder that will generate the API link for a chosen table.
- [UK Data Service](https://ukdataservice.ac.uk/) - ☰ Portal - ○ Open - UK Data Service: curated social and economic data collections for research and teaching, with discovery and download APIs.
- [Bank of England Data](https://www.bankofengland.co.uk/statistics/research-datasets) - ▦ Data - ○ Open - Bank stats and research datasets: interest rates, money and credit, and the Interactive Database with CSV and JSON exports.
- [UK Online Shelf-Price Index](https://data.yappman.com/shelf-price-index) - ▦ Data - ○ Open - Weekly index of online shelf prices at Tesco, Sainsbury's, Asda and Aldi, built from products matched week on week scraped direct from each retailer's site.
- [UK Supermarket Prices: Daily 212-Item Basket](https://www.kaggle.com/datasets/russellyapp/uk-supermarket-prices-daily-212-item-basket) - ▦ Data - ◕ Login - Daily prices for a fixed 212-item grocery basket across Tesco, Sainsbury's, Asda and Aldi, joined on EAN barcode (CC BY 4.0).

## Health and social care

- [NHS England Data](https://digital.nhs.uk/data-and-information/data-tools-and-services) - ▦ Data - ○ Open - NHS England data services: hospital statistics, workforce, GP practice data, and the NHS Digital APIs for health care data.
- [NHSBSA Open Data Portal](https://opendata.nhsbsa.net/) - ☰ Portal - ○ Open - The NHS Business Services Authority open data portal, free to use and reuse under the Open Government Licence. Its themes cover community prescribing and dispensing, dental activity, dispensing contractors, hospital and provider medicines, and digital service performance, alongside ad hoc statistical releases and the FOI disclosure log. Files download as CSV, XLSX, PDF and ZIP, and the portal listed 2,158 packages on 28 September 2026.
- [UKHSA data dashboard](https://ukhsa-dashboard.data.gov.uk/) - ▦ Data - ○ Open - UK Health Security Agency dashboard for public health data in England, covering respiratory viruses, healthcare-associated infections and antimicrobial resistance. The same data is available through a documented API and bulk chart downloads.
- [Care Quality Commission Open Data](https://www.cqc.org.uk/about-us/transparency/using-cqc-data) - ⇄ API - ◑ Key - The Care Quality Commission's data on the health and adult social care services it regulates in England. Its public API at api.service.cqc.org.uk lists every active and inactive provider and location, with the detail behind each one and the links between organisations, refreshed daily; an API key from the CQC developer portal is required. The care directory is also published as spreadsheet downloads. Both are under the Open Government Licence.
- [Fingertips Public Health Profiles](https://fingertips.phe.org.uk/) - ▦ Data - ○ Open - The Office for Health Improvement and Disparities public health data collection for England, part of DHSC. Indicators are grouped into themed profiles that put local figures next to national comparators, with data down to small-area geography. The API answers in JSON or CSV, with R and Python clients, and its endpoint list is documented at /swagger/docs/v1. All content is under the Open Government Licence except where stated.
- [Food Hygiene Rating Scheme API](https://ratings.food.gov.uk/) - ⇄ API - ○ Open - Food Standards Agency food hygiene ratings as a free JSON API: search establishment records and look up local authority details for England, Scotland, Wales and Northern Ireland. No key or sign-up, but every call must send an x-api-version header.

## Environment, climate and geospatial

- [Environment Agency Data](https://environment.data.gov.uk/) - ⇄ API - ○ Open - Environment Agency open data: flood warnings, river levels, water quality, and pollution inventory via environment.data.gov.uk APIs.
- [OS Data Hub](https://osdatahub.os.uk/) - ⇄ API - ◑ Key - Ordnance Survey data APIs: OS Maps, OS Features (address and place data), and OS OpenData products for Great Britain.
- [British Geological Survey OpenGeoscience](https://www.bgs.ac.uk/geological-data/opengeoscience/) - ☰ Portal - ○ Open - BGS geoscience data for the UK: OpenGeoscience publishes maps, borehole log scans, photographs and digital datasets free of charge, alongside WMS and WFS map services, a CSW catalogue for dataset discovery and a download service for geotechnical AGS data. The BGS ArcGIS Open Data Hub carried 72 datasets in its DCAT feed on 27 September 2026. OpenGeoscience data is under the Open Government Licence wherever possible, with a "Contains British Geological Survey materials © UKRI" acknowledgement.
- [Natural England Open Data Geoportal](https://naturalengland-defra.opendata.arcgis.com/) - ☰ Portal - ○ Open - Natural England's open data geoportal on the Defra ArcGIS Hub: more than 250 datasets covering Sites of Special Scientific Interest, National Nature Reserves, the England Coast Path, ancient woodland, moorland change and local nature recovery strategy areas. Each dataset downloads as CSV, Shapefile, GeoJSON, KML, GeoPackage or file geodatabase, and is also served through ArcGIS REST services.
- [Defra UK-AIR (Air Information Resource)](https://uk-air.defra.gov.uk/) - ▦ Data - ○ Open - Defra's air quality data archive: hourly measurements from more than 1,500 monitoring sites across the UK, split into automatic and non-automatic networks, with a data selector for custom extracts and preformatted raw files from the automatic network. Descriptive statistics and exceedance statistics sit alongside the measurements under the Open Government Licence v3.0.
- [Environmental Information Data Centre](https://eidc.ac.uk/) - ☰ Portal - ○ Open - The Environmental Information Data Centre is the UK's national data centre for terrestrial and freshwater sciences, part of the Natural Environment Research Council's Environmental Data Service and hosted by the UK Centre for Ecology & Hydrology. Its catalogue held 2,432 records on 29 September 2026, with topics running from biodiversity and hydrology to land cover and pollution, and it is certified as a trusted repository by CoreTrustSeal. Downloads arrive as zipped data packages, or over plain HTTP for large holdings such as CHESS-met, and the catalogue answers JSON requests directly. Licences are set per record rather than site-wide, so each dataset page states its own terms. From 5 October 2026 programmatic downloads need a Personal Access Token in place of basic authentication.
- [Marine Directorate Data](https://data.marine.gov.scot/) - ☰ Portal - ○ Open - The Marine Directorate of the Scottish Government publishes its marine data through this portal, covering fisheries and aquaculture, marine planning, marine renewables, and freshwater and marine monitoring. The catalogue runs on DKAN, so it is also available as a DCAT data.json feed and a service endpoint, and on 3 October 2026 the feed listed 302 datasets, each with its own licence and a Digital Object Identifier. The portal states that the data is free to download and gives a pre-formatted citation for each record.
- [National River Flow Archive](https://nrfa.ceh.ac.uk/) - ▦ Data - ○ Open - The National River Flow Archive is the UK's official record of river flow data, based at the UK Centre for Ecology & Hydrology and operated on behalf of Defra, the Scottish Government and the Welsh Government. It curates records from more than 1,600 gauging stations, many reaching back to the 1960s, and provides bulk downloads including the Peak Flow Dataset (version 15, released on 27 August 2026) alongside a documented REST API; the station-ids endpoint returned 1,604 stations on 3 October 2026. Access is granted under the NRFA click-through licence, which asks users to acknowledge "Data from the UK National River Flow Archive".
- Met Office
    - [Met Office DataPoint](https://www.metoffice.gov.uk/services/data/datapoint) - ⇄ API - ◑ Key - Met Office open weather API: 3-hourly and daily forecasts, observations, and warnings for UK locations with a free API key.
    - [Met Office Climate Data Portal](https://climatedataportal.metoffice.gov.uk/) - ▦ Data - ○ Open - The Met Office Climate Data Portal publishes the UK's climate observations and projections as downloadable layers and GIS services. Its DCAT feed carried 98 datasets on 1 October 2026, with distributions in ZIP, CSV, GeoJSON, KML, TXT, XLSX, GPKG and GDB, plus an ArcGIS GeoServices REST API for each published layer. The holdings cover monthly and annual temperature, precipitation and wind-speed projections on 12km and 5km grids and at local-authority and sub-local-authority boundaries, sea level projections to 2100, the UK shared socioeconomic pathway scenarios, and gridded observations for 1991 to 2020. Licences are set per dataset, and 89 of the 98 state the Open Government Licence v3.0.
- [SEPA Environmental Data](https://www.sepa.org.uk/environment/environmental-data/) - ▦ Data - ○ Open - Scottish Environment Protection Agency datasets: air, water, waste and flood data, published with CSV, GDB and GeoPackage downloads plus REST and WMS map services.
- [Forest Research statistics](https://www.forestresearch.gov.uk/tools-and-resources/statistics/) - ▦ Data - ○ Open - Forest Research is the research agency of the Forestry Commission and Great Britain's principal organisation for forestry and tree-related research. Its statistics programme publishes official statistics on forestry, from the annual Forestry Statistics to Accredited Official Statistics such as Provisional Woodland Statistics 2026, and it follows the UK Statistics Authority's Code of Practice for Official Statistics. The time series behind those releases, covering woodland area, planting and restocking, wood production and timber prices, is available to download as ODS spreadsheets under the Open Government Licence v3.0.

## Transport

- [TfL Unified API](https://api.tfl.gov.uk/) - ⇄ API - ◑ Key - Transport for London API: live tube, bus, river, and road data, plus arrival predictions, journey plans, and stop information.
- [National Highways Open Data](https://opendata.nationalhighways.co.uk/) - ☰ Portal - ○ Open - National Highways open data services: geographical data about England’s strategic road network, available as downloads or through an API.
- [DVSA MOT History API](https://documentation.history.mot.api.gov.uk/) - ⇄ API - ◑ Key - The MOT history API from the Driver and Vehicle Standards Agency serves vehicle and MOT test records over a JSON REST interface: cars, motorcycles and vans tested in Great Britain since 2005 and Northern Ireland since 2017, plus HGVs, trailers, buses and coaches from Great Britain since 2018 and Northern Ireland from 2017. Access needs a registered API key, the documentation carries its own error codes and rate limits, and a separate page covers bulk downloads of vehicle and MOT history data. All content on the documentation site sits under the Open Government Licence v3.0.
- [Office of Rail and Road Data Portal](https://dataportal.orr.gov.uk/) - ☰ Portal - ○ Open - The Office of Rail and Road publishes its rail statistics on the data portal: passenger and freight usage, performance and cancellations, fares and industry finance, rail safety including the Common Safety Indicators and RIDDOR incident reports, and infrastructure and environment data. Each statistical release carries a set of data tables that download as ODS files, and the portal lists the publication dates for releases ahead. Recent releases include Rail safety, April 2025 to March 2026, published on 24 September 2026, freight rail usage for April to June 2026 on 22 September 2026, and passenger rail performance for the same quarter on 17 September 2026. Material on ORR websites is Crown copyright and available under the Open Government Licence v3.0.

## Energy and utilities

- [NESO Data Portal](https://neso.energy/data-portal) - ☰ Portal - ○ Open - National Energy System Operator open data: generation mix, demand, balancing, and system forecasts for Great Britain.
- [Elexon Insights Solution (BMRS)](https://www.elexon.co.uk/data/) - ⇄ API - ○ Open - The Insights Solution is the open data service for the Balancing Mechanism Reporting Service, covering the electricity system of Great Britain. It publishes generation, demand, balancing and settlement, transmission, and REMIT and operational notices, with a free REST API that returns the data as JSON and a real-time IRIS streaming service alongside it; on 2 October 2026 a call to the generation endpoint returned half-hourly output by fuel type without a key. Elexon describes the service as the replacement for the older BMRS website, and its BMRS open data licence grants worldwide, royalty-free, perpetual and non-exclusive use on condition of the attribution "Contains BMRS data © Elexon Limited copyright and database right [year]".

## Education and research

- [Explore Education Statistics](https://explore-education-statistics.service.gov.uk/) - ▦ Data - ○ Open - Department for Education statistics: school performance, pupil numbers, and early years data with a data explorer API.
- [Office for Students Data and Analysis](https://www.officeforstudents.org.uk/data-and-analysis/) - ▦ Data - ○ Open - The Office for Students is the regulator for higher education in England, and its data and analysis pages carry the statistics behind that role: access and participation, student numbers and characteristics, student outcomes, the National Student Survey and the Teaching Excellence Framework. Interactive dashboards cover the size and shape of provision, student outcomes and TEF ratings, and the releases come with spreadsheet downloads, among them the 2024-25 student numbers table published on 16 September 2026. Content owned by the OfS is available for re-use under the Open Government Licence.
- [UKRI Gateway to Research](https://gtr.ukri.org/) - ⇄ API - ○ Open - Gateway to Research (GtR) is the public catalogue of research and innovation funded by UK Research and Innovation. It indexes projects, organisations, people and outcomes, publishes the award data quarterly in the second week of April, July, October and January, and offers two REST APIs that return the catalogue as JSON without a key; on 2 October 2026 the project endpoint reported 158,710 projects across 15,871 pages of ten, the organisation endpoint 97,102 organisations, and the people endpoint 95,176 people. The site states the data is available under the Open Government Licence.

## Devolved administrations

- Welsh Government
    - [DataMapWales](https://datamap.gov.wales/) - ☰ Portal - ○ Open - Welsh public sector spatial data platform: a catalogue of datasets, maps and apps, with a map viewer, downloads, and direct data access through an API.
    - [StatsWales](https://stats.gov.wales/en-GB) - ▦ Data - ○ Open - Welsh Government statistics about Wales, grouped by topic from health and housing to transport and the Welsh language. The public API lists the published datasets and downloads any of them as JSON, CSV or XLSX.
- Scottish Government
    - [Scottish Government Statistics](https://www.gov.scot/statistics/) - ☰ Portal - ○ Open - The Scottish Government publishes its official statistics and research on gov.scot, listed together in a statistics and research hub that held over 6,000 publications on 1 October 2026. Releases cover the economy, population, health, education, justice, transport, housing and the environment, and most carry spreadsheet tables alongside the report, such as the Excel tables for the quarterly housing statistics update and the Scottish Fish Farm Production Survey. Publications are grouped into collections, among them economy statistics and the fish farm production surveys. Content on gov.scot is available under the Open Government Licence v3.0 except for graphic assets and where stated otherwise.
    - [Scottish Health and Social Care Open Data](https://www.opendata.nhs.scot/) - ☰ Portal - ○ Open - Public Health Scotland’s open data platform: health and social care statistics and reference data under the Open Government Licence, with a CKAN API for bulk access.
- [NISRA Statistics and Research](https://www.nisra.gov.uk/) - ☰ Portal - ○ Open - The Northern Ireland Statistics and Research Agency's statistics hub. NISRA is an executive agency of the Department of Finance (NI) and publishes official statistics on population and the census, health and social care, work, pay and benefits, education and skills, transport, the environment and climate change, crime and justice, and the economy.
- [National Records of Scotland Statistics](https://www.nrscotland.gov.uk/statistics-and-data) - ▦ Data - ○ Open - National Records of Scotland publishes Scotland's official statistics on population, births, deaths, marriages and life expectancy, migration and households, and names, plus the country's census results. Its geography products include the Scottish Postcode Directory, whose index arrives as zipped CSV files with boundary data alongside, and the Scottish Statistics Postcode Lookup. Publications carry downloadable data files, and the site is under the Open Government Licence v3.0.

## Local and regional data

- [London Datastore](https://data.london.gov.uk/) - ☰ Portal - ○ Open - Greater London Authority open data: housing, planning, transport, air quality, and the London Dashboard datasets.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Pull requests are very welcome :smile:.

Tags are checked by the engine, so every entry needs a type (`API`, `Data`, `Portal`, `Register`, `Docs`) and an access level (`Open`, `Key`, `Login`, `Paid`), plus a status (`Legacy`, `Archived`) if the tool has been superseded.

If you spot a dead link, or a link that points at a page instead of the data itself, open an issue or send a PR.

Released under the MIT license, see [LICENSE](LICENSE).
