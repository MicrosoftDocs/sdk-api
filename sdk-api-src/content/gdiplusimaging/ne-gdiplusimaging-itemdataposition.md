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

# ItemDataPosition enumeration


## -description


The <b>ItemDataPosition</b> enumeration is used to specify the location of custom metadata in an image file. 


## -enum-fields




### -field ItemDataPositionAfterHeader

Specifies that custom metadata is stored after the file header. Valid for JPEG, PNG, and GIF.


### -field ItemDataPositionAfterPalette

Specifies that custom metadata is stored after the palette. Valid for PNG.


### -field ItemDataPositionAfterBits

Specifies that custom metadata is stored after the pixel data. Valid for GIF and PNG.


## -remarks



GDI+ supports custom metadata for JPEG, PNG, and GIF image files.




## -see-also




<a href="https://msdn.microsoft.com/56316228-9cae-46d5-bfef-bbd523aabd2b">ImageItemData</a>
 

 

