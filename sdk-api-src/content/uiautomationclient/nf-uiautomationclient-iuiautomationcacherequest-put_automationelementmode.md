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

# IUIAutomationCacheRequest::put_AutomationElementMode


## -description


Indicates whether returned elements contain full references to the underlying UI, or only cached information. 

This property is read/write.


## -parameters


## -remarks



<a href="uiauto_AutomationElementModeEnum.htm">AutomationElementMode_Full</a> is the default value, and specifies that returned elements contain a full reference to the underlying UI. <a href="uiauto_AutomationElementModeEnum.htm">AutomationElementMode_None</a> specifies that the returned elements have no reference to the underlying UI, and contain only cached information.

Certain operations on elements, including <a href="https://msdn.microsoft.com/819e548e-7ff4-4f9f-969b-bfd1625f6151">GetCurrentPropertyValue</a>, and <a href="https://msdn.microsoft.com/4a4e549a-1812-4380-bc0a-2da579a62b5d">SetFocus</a>, require a full reference; attempting to perform these on an element that has none results in an error.

Using <a href="uiauto_AutomationElementModeEnum.htm">AutomationElementMode_None</a> can be more efficient when only properties are needed, as it avoids the overhead involved in setting up full references.



