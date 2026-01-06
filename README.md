# .NET 6 Web API with Hexagonal Architecture
.NET 6 Core applications (console and Web API) example, with hexagonal architecture (ports and adapters). It includes unit, integration and architectural tests too.

## About the solution
Hexagonal architecture helps to visualize the solution global workflow because it is implicit in its organization: 

The solution has:
- Two in-adapters corresponding to executable assemblies. These adapters interact with the application (NetCoreHexagonal.Application) using an in-port.
- One in-port: ISchoolService.
- One in-port implementation: SchoolService. This implementation interacts with external services that fullfill two out-ports.
- Two out-ports defined with interfaces in folders EventsDispatching and Persistence.
- Two out-adapters implementing each out-port.
