## Each section is an object in YAML
## YAML syntax https://learnxinyminutes.com/docs/yaml/
## https://github.com/OAI/OpenAPI-Specification/tree/master/
## https://github.com/OAI/OpenAPI-Specification/blob/master/versions/3.0.2.md
## Objects https://github.com/OAI/OpenAPI-Specification/blob/master/versions/3.0.2.md#fixed-fields
## Obder brother of OA3 Swagger docs: https://swagger.io/docs/specification/about/
## version, info and paths is required
## Sections of OA3
#### Field Name 	Type 	Description
#### openapi 	string 	REQUIRED. This string MUST be the semantic version number of the OpenAPI Specification version that the OpenAPI document uses. The openapi field SHOULD be used by tooling specifications and clients to interpret the OpenAPI document. This is not related to the API info.version string.
#### info 	Info Object 	REQUIRED. Provides metadata about the API. The metadata MAY be used by tooling as required.
#### servers 	[Server Object] 	An array of Server Objects, which provide connectivity information to a target server. If the servers property is not provided, or is an empty array, the default value would be a Server Object with a url value of /.
#### paths 	Paths Object 	REQUIRED. The available paths and operations for the API.
#### components 	Components Object 	An element to hold various schemas for the specification.
#### security 	[Security Requirement Object] 	A declaration of which security mechanisms can be used across the API. The list of values includes alternative security requirement objects that can be used. Only one of the security requirement objects need to be satisfied to authorize a request. Individual operations can override this definition.
#### tags 	[Tag Object] A list of tags used by the specification with additional metadata. The order of the tags can be used to reflect on their order by the parsing tools. Not all tags that are used by the Operation Object must be declared. The tags that are not declared MAY be organized randomly or based on the tools' logic. Each tag name in the list MUST be unique.
#### externalDocs 	External Documentation Object 	Additional external documentation.
## YAML clossly matches https://json-schema.org/understanding-json-schema/index.html to json types and patterns
### Json Schema is Last updated on Apr 12, 2020.
### component schema reference can be in either
- same file "$ref": "#/components/schema/pet"
- local json file "$ref": "Pet.json"
- local yaml file "$ref": Pet.yaml
- one defenition file with references in it "$ref": "defenitions.json#pet"
### Parameter https://github.com/OAI/OpenAPI-Specification/blob/master/versions/3.0.2.md#fixed-fields-10
- path
- query
- header
- cookie
## Summary and description is more important when sharing the API
## OAS supports markdown
## tags are logical grouping
## operation id is going to used in codegens and it has following props
- case-sensitive
- must be unique
- recommende to follow programming practices

## readOnly property readonly is a property which says it should not be supplied by the requester but may or may not be set by the server it is opposite of writeOnly
## delete should return 200 for successfully deletion
## 409 status code is used to indicate a state of conflict
## Callback is an event when we need to respond to that event exemple send a notification to some server
### https://swagger.io/docs/specification/callbacks/
### https://swagger.io/docs/specification/about/

## Security scheme object "https://github.com/OAI/OpenAPI-Specification/blob/master/versions/3.0.2.md#securitySchemeObject"
## Security scheme swagger docs https://swagger.io/docs/specification/authentication/

# Codegenerator
## One way - https://openapi-generator.tech/
