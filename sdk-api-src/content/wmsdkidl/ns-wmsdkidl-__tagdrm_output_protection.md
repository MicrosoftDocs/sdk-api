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

# __tagDRM_OUTPUT_PROTECTION structure


## -description



The <b>DRM_VIDEO_OUTPUT_PROTECTION</b> structure holds a video output technology identifier and the configuration data required by that technology.




## -struct-fields




### -field guidId

Technology identifier.


### -field bConfigData

Configuration data required by the technology identified by <b>guidId</b>.


## -remarks



The <a href="https://msdn.microsoft.com/95bce5f8-5230-4b69-b4e9-3cb766edce90">DRM_VIDEO_OUTPUT_PROTECTION_IDS</a> structure contains an array of <b>DRM_VIDEO_OUTPUT_PROTECTION</b> structures.




## -see-also




<a href="https://msdn.microsoft.com/95bce5f8-5230-4b69-b4e9-3cb766edce90">DRM_VIDEO_OUTPUT_PROTECTION_IDS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

