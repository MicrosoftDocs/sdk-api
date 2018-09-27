---
UID: NS:d2d1effectauthor.D2D1_BLEND_DESCRIPTION
title: D2D1_BLEND_DESCRIPTION
author: windows-sdk-content
description: Defines a blend description to be used in a particular blend transform.
old-location: direct2d\d2d1_blend_description.htm
tech.root: direct2d
ms.assetid: 5f4c7248-9303-4451-92f1-4b230efd627a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D2D1_BLEND_DESCRIPTION, D2D1_BLEND_DESCRIPTION structure [Direct2D], d2d1effectauthor/D2D1_BLEND_DESCRIPTION, direct2d.d2d1_blend_description
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: D2d1.lib; D2d1.dll
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2d1.lib
 - D2d1.dll
api_name:
 - D2D1_BLEND_DESCRIPTION
product: Windows
targetos: Windows
req.typenames: D2D1_BLEND_DESCRIPTION
req.redist: 
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
 

 

