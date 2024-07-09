# apidoc-swagger
> A open source library that generate your API documentation in a separated file.

## Client Usage.
> Follow the below steps to generate your API documentation.


### Install apidoc-swagger library into your project.

### Step - 1:
Go to your project root directory and run below command.

For npm users, execute the following command:

```sh
npm install apidoc-swagger --save -dev
```

Alternatively Yarn users, execute the following command:

```sh
yarn add apidoc-swagger --save -dev
```
### Step - 2:
A pop up is open in console as like as below. Select langugae and/or press enter. By default it is Typescript.
```text
Language Type -> Typescript
              -> Javascript

```

### Step - 3:
A pop up is open in console as like as below. Select framework and/or press enter. By default it is Express.
```text
Framework Type -> Express
               -> Nest
               -> Fastify
```
### Step - 4:
A pop up is open in console as like as below. Select document type and/or press enter. By default it is Swagger.
```text
Document Type  -> Swagger documentation
               -> Postman collection
               -> Pdf Documentation
```

### Step - 5:
Go to 'document/config.(ts/js)' And modify this based on requirements.
```sh
// document/config.(ts/js)
{
    project_name: "test-1",
    project_version: "1.0.1",
    language: "Typescript",
    framewrk: "express",
    tag: "Backend",
    date: Date.now(),
    document_type: ["swagger",...]
    schema_route_mapper: [
        {
            route_path: "",
            schema_path: "",
            exclude_fields: ['name',...],
            include_fields:[
                {
                    name: "name",
                    type: "string",
                    max_length: 120,
                    min_length: 12,
                    default_value: 110,
                    is_unique: false,
                    example: "Hello",
                    required: true
                }
            ]
        }
    ]
}
```