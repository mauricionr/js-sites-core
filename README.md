# JS Sites Core
SharePoint Provisioning engine with pure JavaScript inspired by https://github.com/OfficeDev/PnP-Sites-Core/

# Using js-sites-core
Can be as simple as
```
jQuery.getScript(`${_spPageContextInfo.siteAbsoluteUrl}/SiteAssets/js/pzl.sites.core.js`, () => {
    Pzl.Sites.Core.init(siteTemplateConfig, { "Logging": { "On": true } }).then(() => {               
        
    })
});
```

or with logging to file

```
jQuery.getScript(`${_spPageContextInfo.siteAbsoluteUrl}/SiteAssets/js/pzl.sites.core.js`, () => {
    Pzl.Sites.Core.init(siteTemplateConfig, { "Logging": { "On": true, "LoggingFolder": _spPageContextInfo.siteServerRelativeUrl + "/SiteAssets/logs" } }).then(() => {               
        
    })
});
```

with customized wait message

```
jQuery.getScript(`${_spPageContextInfo.siteAbsoluteUrl}/SiteAssets/js/pzl.sites.core.js`, () => {
    Pzl.Sites.Core.init(siteTemplateConfig, 
    { 
        "WaitMessage": { "Header": "Working on it..", "Content": "Won't take long mate!" },  
        "Logging": { "On": true, "LoggingFolder": _spPageContextInfo.siteServerRelativeUrl + "/SiteAssets/logs" } 
    }
    ).then(() => {               
        
    })
});
```
# Bower
js-sites-core is available through bower.

Package information
```powershell
    bower info js-sites-core
```

Install package
```powershell
    bower install js-sites-core
```

# Schema
Schema is inspired by https://github.com/OfficeDev/PnP-Provisioning-Schema

Most of the differences are due to the available CSOM attributes and functions.

[Schema](dist/schema.md)

# Samples
[Full Sample](samples/Full-Sample.md)
