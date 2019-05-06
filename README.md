# webim
Sharing the progress and feature list for the webim project.

The public mirror for https://github.com/yanweizh/webim

## Features List

- [ ] The overall Solution/Project architecture management implementation
     - [ ] The outermost set is called a `Solution`
     - [ ] Inside a `Solution` there can be multiple `Project`s
     - [ ] Inside every `Project` there are many `Categories`
     - [ ] Every `Category` can contain multiple IFC files
     - [ ] (Optional) Every IFC file can have version 
- [ ] Multiple projects load support
     - [ ] Merge "Load" & "Federation Load" logic, 
     - [ ] Support multiple tree view navigate for loaded `IFCStore` models
- [ ] Support searching
     - [ ] Searching UI dialog implementation
     - [ ] Searching logic ViewModel
     - [x] Searching result & 3D model integration 
- [ ] Property Edit
     - [ ] Aggregate the properties that need to be editable
     - [ ] Able to edit properties and set the properties back to the model with "version", so that the "version" can be used when merging with updated .ifc files
     - [ ] Able to detect and refuse invalid properties
- [ ] IFC model update
     - [ ] Model update UI dialog implementation
     - [ ] The merging logic implentation
        - [ ] When there is not GUID matching for models, report warning and reload a new model?
        - [ ] When there is partial GUID matching for models, able to list the updated/deleted/added/conflict model parts
        - [ ] When there is no conflict, show the result and complete
        - [ ] For conflicts, if the model property is updated from our WeBim app, and in the meanwhile, is updated from the newly imported IFC file
- [ ] (Optional) Publish the IFC model and view it from URL
      - [ ] Able to publish the IFC model to an Azure Blob ( Public) or a REST API Web App with JWT Authentication (have expire time)
      - [ ] With url `<host>/<model_path>/token=<token>` one can view the model rendered by WebGL, engine can be [xbimWebUI](https://github.com/xBimTeam/XbimWebUI)
