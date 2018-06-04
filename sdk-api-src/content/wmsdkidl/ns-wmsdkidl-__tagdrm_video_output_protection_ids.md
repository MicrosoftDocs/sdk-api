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

# __tagDRM_VIDEO_OUTPUT_PROTECTION_IDS structure


## -description



The <b>DRM_VIDEO_OUTPUT_PROTECTION_IDS</b> structure holds an array of <a href="https://msdn.microsoft.com/73c7b2ab-3680-462a-ab7f-d3270ea0127b">DRM_VIDEO_OUTPUT_PROTECTION</a> structures.




## -struct-fields




### -field cEntries

Number of elements in the array referenced by <b>rgVop</b>.


### -field rgVop

Address of an array of <b>DRM_VIDEO_OUTPUT_PROTECTION</b> structures.


## -remarks



This structure is used as a member of the <a href="https://msdn.microsoft.com/5d14bd02-0fb5-4982-b3dc-7f8277cb852f">DRM_PLAY_OPL</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/73c7b2ab-3680-462a-ab7f-d3270ea0127b">DRM_VIDEO_OUTPUT_PROTECTION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

