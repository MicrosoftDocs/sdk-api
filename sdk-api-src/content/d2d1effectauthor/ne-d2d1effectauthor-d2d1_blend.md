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

# D2D1_BLEND enumeration


## -description


Specifies how one of the color sources is to be derived and optionally specifies a preblend operation on the color source.


## -enum-fields




### -field D2D1_BLEND_ZERO

The data source is black (0, 0, 0, 0). There is no preblend operation.


### -field D2D1_BLEND_ONE

The data source is white (1, 1, 1, 1). There is no preblend operation.


### -field D2D1_BLEND_SRC_COLOR

The data source is color data (RGB) from the second input of the blend transform. There is not a preblend operation.


### -field D2D1_BLEND_INV_SRC_COLOR

The data source is color data (RGB) from second input of the blend transform. The preblend operation inverts the data, generating 1 - RGB.


### -field D2D1_BLEND_SRC_ALPHA

The data source is alpha data (A) from second input of the blend transform. There is no preblend operation.


### -field D2D1_BLEND_INV_SRC_ALPHA

The data source is alpha data (A) from the second input of the blend transform. The preblend operation inverts the data, generating 1 - A.


### -field D2D1_BLEND_DEST_ALPHA

The data source is alpha data (A) from the first input of the blend transform. There is no preblend operation.


### -field D2D1_BLEND_INV_DEST_ALPHA

The data source is alpha data (A) from the first input of the blend transform. The preblend operation inverts the data, generating 1 - A.


### -field D2D1_BLEND_DEST_COLOR

The data source is color data from the first input of the blend transform. There is no preblend operation.


### -field D2D1_BLEND_INV_DEST_COLOR

The data source is color data from the first input of the blend transform. The preblend operation inverts the data, generating 1 - RGB.


### -field D2D1_BLEND_SRC_ALPHA_SAT

The data source is alpha data from the second input of the blend transform. The preblend operation clamps the data to 1 or less.


### -field D2D1_BLEND_BLEND_FACTOR

The data source is the blend factor. There is no preblend operation.


### -field D2D1_BLEND_INV_BLEND_FACTOR

The data source is the blend factor. The preblend operation inverts the blend factor, generating 1 - blend_factor.


### -field D2D1_BLEND_FORCE_DWORD




## -remarks



This enumeration has the same numeric values as <a href="https://msdn.microsoft.com/0d3a337d-3d16-4a0a-9611-b511c8fb39b4">D3D10_BLEND</a>.




## -see-also




<a href="https://msdn.microsoft.com/5f4c7248-9303-4451-92f1-4b230efd627a">D2D1_BLEND_DESCRIPTION</a>



<a href="https://msdn.microsoft.com/0DC46758-6005-4A33-9539-9C95CF8CFB6A">ID2D1BlendTransform</a>
 

 

