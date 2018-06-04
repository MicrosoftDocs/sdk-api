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

# D2D1_MAP_OPTIONS enumeration


## -description


Specifies how the memory to be mapped from the corresponding <a href="https://msdn.microsoft.com/669a9377-248c-4a86-b447-ed117fff43a6">ID2D1Bitmap1</a> should be treated.


## -enum-fields




### -field D2D1_MAP_OPTIONS_NONE


### -field D2D1_MAP_OPTIONS_READ

Allow CPU Read access.


### -field D2D1_MAP_OPTIONS_WRITE

Allow CPU Write access.


### -field D2D1_MAP_OPTIONS_DISCARD

Discard the previous contents of the resource when it is mapped.


### -field D2D1_MAP_OPTIONS_FORCE_DWORD




## -remarks



The <b>D2D1_MAP_OPTIONS_READ</b> option can be used only if the bitmap was created with the <b>D2D1_BITMAP_OPTIONS_CPU_READ</b> flag.

These flags will be not be able to be used on bitmaps created by the <a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>. However, the ID2D1SourceTransform will receive bitmaps for which these flags are valid.

<b>D2D1_MAP_OPTIONS_DISCARD</b> can only be used with <b>D2D1_MAP_OPTIONS_WRITE</b>.  Both of these options are only available through the effect author API, not through the Direct2D rendering API.





## -see-also




<a href="https://msdn.microsoft.com/284c16ea-1a9f-4f13-b359-214178650add">ID2D1Bitmap1::Map</a>
 

 

