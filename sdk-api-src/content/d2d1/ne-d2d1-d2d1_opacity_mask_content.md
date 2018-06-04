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

# D2D1_OPACITY_MASK_CONTENT enumeration


## -description


Describes whether an opacity mask contains graphics or text. Direct2D uses this information to determine which gamma space to use when blending the opacity mask.


## -enum-fields




### -field D2D1_OPACITY_MASK_CONTENT_GRAPHICS

The opacity mask contains graphics. The opacity mask is blended in the gamma 2.2 color space.


### -field D2D1_OPACITY_MASK_CONTENT_TEXT_NATURAL

The opacity mask contains non-GDI text. The gamma space used for blending is obtained from the render target's text rendering parameters. (<a href="https://msdn.microsoft.com/ab4b29a5-72a7-49dc-9131-696f888b0355">ID2D1RenderTarget::SetTextRenderingParams</a>).


### -field D2D1_OPACITY_MASK_CONTENT_TEXT_GDI_COMPATIBLE

The opacity mask contains text rendered using the GDI-compatible rendering mode. The opacity mask is blended using the gamma for GDI rendering.


### -field D2D1_OPACITY_MASK_CONTENT_FORCE_DWORD




## -see-also




<a href="https://msdn.microsoft.com/b55cc9f3-7378-4ffd-bc71-8e06a2fb9f9e">FillOpacityMask</a>
 

 

