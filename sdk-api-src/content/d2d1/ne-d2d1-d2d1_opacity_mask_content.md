---
UID: NE:d2d1.D2D1_OPACITY_MASK_CONTENT
title: D2D1_OPACITY_MASK_CONTENT (d2d1.h)
author: windows-sdk-content
description: Describes whether an opacity mask contains graphics or text. Direct2D uses this information to determine which gamma space to use when blending the opacity mask.
old-location: direct2d\d2d1_opacity_mask_content.htm
tech.root: Direct2D
ms.assetid: ea14d7eb-b8cc-4ab8-8f51-9174748ee6a2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D2D1_OPACITY_MASK_CONTENT, D2D1_OPACITY_MASK_CONTENT enumeration [Direct2D], D2D1_OPACITY_MASK_CONTENT_GRAPHICS, D2D1_OPACITY_MASK_CONTENT_TEXT_GDI_COMPATIBLE, D2D1_OPACITY_MASK_CONTENT_TEXT_NATURAL, d2d1/D2D1_OPACITY_MASK_CONTENT, d2d1/D2D1_OPACITY_MASK_CONTENT_GRAPHICS, d2d1/D2D1_OPACITY_MASK_CONTENT_TEXT_GDI_COMPATIBLE, d2d1/D2D1_OPACITY_MASK_CONTENT_TEXT_NATURAL, direct2d.d2d1_opacity_mask_content
ms.topic: enum
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_OPACITY_MASK_CONTENT
product: Windows
targetos: Windows
req.typenames: D2D1_OPACITY_MASK_CONTENT
req.redist: 
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
 

 

