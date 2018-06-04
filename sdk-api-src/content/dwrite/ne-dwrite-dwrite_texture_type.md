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

# DWRITE_TEXTURE_TYPE enumeration


## -description


Identifies a type of alpha texture.


## -enum-fields




### -field DWRITE_TEXTURE_ALIASED_1x1

Specifies an alpha texture for aliased text rendering (that is,  each pixel is either fully opaque or fully transparent), with one byte per pixel.


### -field DWRITE_TEXTURE_CLEARTYPE_3x1

Specifies an alpha texture for ClearType text rendering, with three bytes per pixel in the horizontal dimension and one byte per pixel in the vertical dimension.


## -remarks



An alpha texture is a bitmap of alpha values, each representing opacity of a pixel or subpixel.



