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

# tagMETAFILEPICT structure


## -description


Defines the metafile picture format used for exchanging metafile data through the clipboard. 


## -struct-fields




### -field mm

Type: <b>LONG</b>

The mapping mode in which the picture is drawn. 


### -field xExt

Type: <b>LONG</b>

The size of the metafile picture for all modes except the <b>MM_ISOTROPIC</b> and <b>MM_ANISOTROPIC</b> modes. (For more information about these modes, see the <b>yExt</b> member.) The x-extent specifies the width of the rectangle within which the picture is drawn. The coordinates are in units that correspond to the mapping mode. 


### -field yExt

Type: <b>LONG</b>

The size of the metafile picture for all modes except the <b>MM_ISOTROPIC</b> and <b>MM_ANISOTROPIC</b> modes. The y-extent specifies the height of the rectangle within which the picture is drawn. The coordinates are in units that correspond to the mapping mode. For <b>MM_ISOTROPIC</b> and <b>MM_ANISOTROPIC</b> modes, which can be scaled, the <b>xExt</b> and <b>yExt</b> members contain an optional suggested size in <b>MM_HIMETRIC</b> units. For <b>MM_ANISOTROPIC</b> pictures, <b>xExt</b> and <b>yExt</b> can be zero when no suggested size is supplied. For <b>MM_ISOTROPIC</b> pictures, an aspect ratio must be supplied even when no suggested size is given. (If a suggested size is given, the aspect ratio is implied by the size.) To give an aspect ratio without implying a suggested size, set <b>xExt</b> and <b>yExt</b> to negative values whose ratio is the appropriate aspect ratio. The magnitude of the negative <b>xExt</b> and <b>yExt</b> values is ignored; only the ratio is used. 


### -field hMF

Type: <b>HMETAFILE</b>

A handle to a memory metafile. 


## -see-also




<a href="https://msdn.microsoft.com/61a9bff7-3c46-4e42-81f7-e020ff0b667f">Clipboard</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/45ca0c04-cf1a-4206-a05f-9957e50be89c">SetClipboardData</a>
 

 

