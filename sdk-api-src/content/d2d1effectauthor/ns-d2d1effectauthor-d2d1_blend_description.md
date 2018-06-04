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

# D2D1_BLEND_DESCRIPTION structure


## -description


Defines a blend description to be used in a particular blend transform.


## -struct-fields




### -field sourceBlend

Specifies the first RGB data source and includes an optional preblend operation.


### -field destinationBlend

Specifies the second RGB data source and includes an optional preblend operation.


### -field blendOperation

Specifies how to combine the RGB data sources.


### -field sourceBlendAlpha

Specifies the first alpha data source and includes an optional preblend operation. Blend options that end in _COLOR are not allowed.


### -field destinationBlendAlpha

Specifies the second alpha data source and includes an optional preblend operation. Blend options that end in _COLOR are not allowed.


### -field blendOperationAlpha

Specifies how to combine the alpha data sources.


### -field blendFactor

Parameters to the blend operations. The blend must use <b>D2D1_BLEND_BLEND_FACTOR</b> for this to be used.


## -remarks



This description closely matches the <a href="https://msdn.microsoft.com/388f862c-58b0-48a8-a865-ba7568484ef5">D3D11_BLEND_DESC</a> struct with some omissions and the addition of the blend factor in the description.




## -see-also




<a href="https://msdn.microsoft.com/9bc91efd-f695-4bc6-a63e-a3862cca91dd">D2D1_BLEND</a>



<a href="https://msdn.microsoft.com/54977cf3-cca3-4a1e-a039-1ee4a8d44686">D2D1_BLEND_OPERATION</a>
 

 

