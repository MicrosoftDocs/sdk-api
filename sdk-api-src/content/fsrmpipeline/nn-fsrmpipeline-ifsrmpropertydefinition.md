---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IFsrmPropertyDefinition interface


## -description


Defines a property that you want to use to classify files.

To create this interface, call the 
    <a href="https://msdn.microsoft.com/92c6198b-08b6-4ea6-b8de-1a21acd235d1">IFsrmClassificationManager::CreatePropertyDefinition</a> 
    method.

The following methods return this interface:
<ul>
<li>
<a href="https://msdn.microsoft.com/c97cb2f1-6e03-444e-a15e-faa85f7a7915">IFsrmClassificationManager::EnumPropertyDefinitions</a>
</li>
<li>
<a href="https://msdn.microsoft.com/de89524d-70b7-4f0a-add0-d34d54bd32a7">IFsrmClassificationManager::GetPropertyDefinition</a>
</li>
</ul>

## -remarks



The name and type properties define a unique property; you cannot rename a property or change its type.

You cannot delete a property definition that is referenced by a classification rule or report. The 
    classification rule uses the 
    <a href="https://msdn.microsoft.com/0e41ac2b-c48a-4bb8-a363-8a64c856b8f9">IFsrmRule::PropertyAffected</a> 
    property to reference the property definition.

You cannot delete a property  that is referenced by a file management job property condition. To determine if 
    a property condition is holding a reference, look for property conditions that have the "name" 
    property of the condition equal to the name of the property definition that is being deleted.

Reports use the property definition only as a filter in the report type 
    <b>FsrmReportType_FilesByProperty</b>.


#### Examples

For examples in C# and PowerShell see 
     <a href="https://msdn.microsoft.com/E057898F-72A0-4AB0-BE88-4C1BE6B2B5DE">Accessing Classification Properties</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/bb08ea40-6f0e-4ad5-ad57-78f17bbbd4b7">IFsrmObject</a>



<a href="https://msdn.microsoft.com/feffccd1-cf72-45c0-97b3-d6efd736223e">IFsrmProperty</a>
 

 

