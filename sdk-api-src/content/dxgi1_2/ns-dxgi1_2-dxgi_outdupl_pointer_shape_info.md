---
UID: NS:dxgi1_2.DXGI_OUTDUPL_POINTER_SHAPE_INFO
title: DXGI_OUTDUPL_POINTER_SHAPE_INFO (dxgi1_2.h)
description: The DXGI_OUTDUPL_POINTER_SHAPE_INFO structure describes information about the cursor shape.
old-location: direct3ddxgi\dxgi_outdupl_pointer_shape_info.htm
tech.root: direct3ddxgi
ms.assetid: 8C270C30-01B8-467C-939F-7F4B82B9ED15
ms.date: 12/05/2018
ms.keywords: DXGI_OUTDUPL_POINTER_SHAPE_INFO, DXGI_OUTDUPL_POINTER_SHAPE_INFO structure [DXGI], direct3ddxgi.dxgi_outdupl_pointer_shape_info, dxgi1_2/DXGI_OUTDUPL_POINTER_SHAPE_INFO
f1_keywords:
- dxgi1_2/DXGI_OUTDUPL_POINTER_SHAPE_INFO
dev_langs:
- c++
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps only]
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
- DXGI1_2.h
api_name:
- DXGI_OUTDUPL_POINTER_SHAPE_INFO
targetos: Windows
req.typenames: DXGI_OUTDUPL_POINTER_SHAPE_INFO
req.redist: 
ms.custom: 19H1
---

# DXGI_OUTDUPL_POINTER_SHAPE_INFO structure


## -description


The <b>DXGI_OUTDUPL_POINTER_SHAPE_INFO</b> structure describes information about the cursor shape.


## -struct-fields




### -field Type

A <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_outdupl_pointer_shape_type">DXGI_OUTDUPL_POINTER_SHAPE_TYPE</a>-typed value that specifies the type of cursor shape. 


### -field Width

The width in pixels of the mouse cursor.


### -field Height

The height in scan lines of the mouse cursor.


### -field Pitch

The width in bytes of the mouse cursor.


### -field HotSpot

The position of the cursor's hot spot relative to its upper-left pixel. An application does not use the hot spot when it determines where to draw the cursor shape.


## -remarks



An application draws the cursor shape with the top-left-hand corner drawn at the position that the <b>Position</b> member of the  <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_outdupl_pointer_position">DXGI_OUTDUPL_POINTER_POSITION</a> structure specifies; the application does not use the hot spot to draw the cursor shape.

An application calls the  <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape">IDXGIOutputDuplication::GetFramePointerShape</a> method to retrieve cursor shape information in a  <b>DXGI_OUTDUPL_POINTER_SHAPE_INFO</b> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape">IDXGIOutputDuplication::GetFramePointerShape</a>
 

 

