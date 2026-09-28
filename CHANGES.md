# Changelog

Notable changes to the ThingWorx Proficy Historian API Building Block are documented in this file.

## [0.1.1] - 2026-09-28

- Added `GetHistorianTags` service to retrieve all Historian tags
- Breaking changes to `QueryHistorianSingleTag`, `QueryHistorianMultipleTags`, `GetHistorianTagMax`, and `GetHistorianTagMin`
  - Input is now a generic `tagName` (if using the previous sample structure, build that structure elsewhere before calling these services)
  - Output is now the `TWSC.ProficyHistorianAPI.Sample_DS` for Query services
  - Added consistent sorting of query results by timestamp
- `GetHistorianEntities` & `GetHistorianEntityTags`: moved constant for delimiter to a parameter with a default of ">"
- Fixed `GetHistorianTagMin` to return LoEng Units correctly

## [0.1.0] - 2026-09-23

- Initial release of the Proficy Historian REST API Building Block for ThingWorx.
- OAuth token retrieval through `GetOAuthToken`.
- Reusable Historian REST API request execution through `ExecuteRequest`.
- Request parameter discovery through `GetParametersFromRequest`.
- Request specification generation through `GetRequestSpecification`.
- Parameterized request specification generation through `GetRequestSpecificationWithParameters`.
- Example services for retrieving maximum and minimum Historian tag values through `GetHistorianTagMax` and `GetHistorianTagMin`.
- README documentation covering prerequisites, configuration, services, and example usage.
