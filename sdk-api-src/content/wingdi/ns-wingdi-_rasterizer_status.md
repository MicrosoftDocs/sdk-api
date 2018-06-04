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

# _RASTERIZER_STATUS structure


## -description



The <b>RASTERIZER_STATUS</b> structure contains information about whether TrueType is installed. This structure is filled when an application calls the <a href="https://msdn.microsoft.com/0898d1c0-5480-4bd2-aa45-918340172a05">GetRasterizerCaps</a> function.




## -struct-fields




### -field nSize

The size, in bytes, of the <b>RASTERIZER_STATUS</b> structure.


### -field wFlags

Specifies whether at least one TrueType font is installed and whether TrueType is enabled. This value is TT_AVAILABLE, TT_ENABLED, or both if TrueType is on the system.


### -field nLanguageID

The language in the system's Setup.inf file.


## -see-also




<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/0898d1c0-5480-4bd2-aa45-918340172a05">GetRasterizerCaps</a>
 

 

