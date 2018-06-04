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

# D2D1_DEBUG_LEVEL enumeration


## -description


Indicates the type of information provided by the <a href="https://msdn.microsoft.com/7c28e00b-ebb9-4b79-939c-64eade1351ad">Direct2D Debug Layer</a>.  


## -enum-fields




### -field D2D1_DEBUG_LEVEL_NONE

Direct2D does not produce any debugging output. 


### -field D2D1_DEBUG_LEVEL_ERROR

Direct2D sends error messages to the debug layer.


### -field D2D1_DEBUG_LEVEL_WARNING

Direct2D sends error messages and warnings to the debug layer.


### -field D2D1_DEBUG_LEVEL_INFORMATION

Direct2D sends error messages, warnings, and additional diagnostic information that can help improve performance to the debug layer.  


### -field D2D1_DEBUG_LEVEL_FORCE_DWORD




## -remarks



To receive debugging messages, you must install the <a href="https://msdn.microsoft.com/7c28e00b-ebb9-4b79-939c-64eade1351ad">Direct2D Debug Layer</a>.




## -see-also




<a href="https://msdn.microsoft.com/2765d34e-978c-4121-82c9-2780d54e2850">D2D1_FACTORY_OPTIONS</a>



<a href="https://msdn.microsoft.com/7c28e00b-ebb9-4b79-939c-64eade1351ad">Direct2D Debug Layer</a>
 

 

