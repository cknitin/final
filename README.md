## ASP.NET Request Processing Flow (.Net Framework)

 `Client Request
      ↓
 IIS (Handler Mapping)
      ↓
 ISAPI Extension (aspnet_isapi.dll)
      ↓
 ASP.NET Pipeline
      ├── BeginRequest
      ├── AuthenticateRequest
      ├── AuthorizeRequest
      ├── ResolveRequestCache
      ↓
 HTTP Handler (PageHandlerFactory for .aspx)
      ↓
 Page Lifecycle
      ├── Init
      ├── Load
      ├── PreRender
      ├── Render
      └── Unload
      ↓
 ASP.NET Pipeline
      ├── UpdateRequestCache
      └── EndRequest
      ↓
 IIS
      ↓
 Client Receives Response`
