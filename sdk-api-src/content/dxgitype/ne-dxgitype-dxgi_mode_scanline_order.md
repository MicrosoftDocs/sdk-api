---
UID: NE:dxgitype.DXGI_MODE_SCANLINE_ORDER
title: DXGI_MODE_SCANLINE_ORDER
author: windows-sdk-content
description: Flags indicating the method the raster uses to create an image on a surface.
old-location: direct3ddxgi\DXGI_MODE_SCANLINE_ORDER.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\dxgi_mode_scanline_order.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: 743b2fc8-57ea-615d-8363-6e80675a749f, DXGI_MODE_SCANLINE_ORDER, DXGI_MODE_SCANLINE_ORDER enumeration [DXGI], DXGI_MODE_SCANLINE_ORDER_LOWER_FIELD_FIRST, DXGI_MODE_SCANLINE_ORDER_PROGRESSIVE, DXGI_MODE_SCANLINE_ORDER_UNSPECIFIED, DXGI_MODE_SCANLINE_ORDER_UPPER_FIELD_FIRST, direct3ddxgi.DXGI_MODE_SCANLINE_ORDER, dxgitype/DXGI_MODE_SCANLINE_ORDER, dxgitype/DXGI_MODE_SCANLINE_ORDER_LOWER_FIELD_FIRST, dxgitype/DXGI_MODE_SCANLINE_ORDER_PROGRESSIVE, dxgitype/DXGI_MODE_SCANLINE_ORDER_UNSPECIFIED, dxgitype/DXGI_MODE_SCANLINE_ORDER_UPPER_FIELD_FIRST
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: dxgitype.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: DXGI_MODE_SCANLINE_ORDER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgitype.h
api_name:
 - DXGI_MODE_SCANLINE_ORDER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DXGI_MODE_SCANLINE_ORDER enumeration


## -description


Flags indicating the method the raster uses to create an image on a surface.


## -enum-fields




### -field DXGI_MODE_SCANLINE_ORDER_UNSPECIFIED

Scanline order is unspecified.


### -field DXGI_MODE_SCANLINE_ORDER_PROGRESSIVE

The image is created from the first scanline to the last without skipping any.


### -field DXGI_MODE_SCANLINE_ORDER_UPPER_FIELD_FIRST

The image is created beginning with the upper field.


### -field DXGI_MODE_SCANLINE_ORDER_LOWER_FIELD_FIRST

The image is created beginning with the lower field.


## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/8F44CF77-D3A1-44F7-AB7F-69E5727A4378">DXGI_MODE_DESC1</a> and <a href="https://msdn.microsoft.com/0EE5683E-0623-4FD7-A77F-B64F90A25C6A">DXGI_SWAP_CHAIN_FULLSCREEN_DESC</a> structures.




## -see-also




<a href="https://msdn.microsoft.com/c4574c89-dee2-4841-9318-5383cf417111">DXGI Enumerations</a>
 

 

