---
UID: NS:dxgi1_2.DXGI_OUTDUPL_MOVE_RECT
title: DXGI_OUTDUPL_MOVE_RECT (dxgi1_2.h)
description: The DXGI_OUTDUPL_MOVE_RECT structure describes the movement of a rectangle.
helpviewer_keywords: ["DXGI_OUTDUPL_MOVE_RECT","DXGI_OUTDUPL_MOVE_RECT structure [DXGI]","direct3ddxgi.dxgi_outdupl_move_rect","dxgi1_2/DXGI_OUTDUPL_MOVE_RECT"]
old-location: direct3ddxgi\dxgi_outdupl_move_rect.htm
tech.root: direct3ddxgi
ms.assetid: B19DB70A-83B4-4683-9E9B-3DA5D33AB564
ms.date: 12/05/2018
ms.keywords: DXGI_OUTDUPL_MOVE_RECT, DXGI_OUTDUPL_MOVE_RECT structure [DXGI], direct3ddxgi.dxgi_outdupl_move_rect, dxgi1_2/DXGI_OUTDUPL_MOVE_RECT
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
targetos: Windows
req.typenames: DXGI_OUTDUPL_MOVE_RECT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_OUTDUPL_MOVE_RECT
 - dxgi1_2/DXGI_OUTDUPL_MOVE_RECT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI1_2.h
api_name:
 - DXGI_OUTDUPL_MOVE_RECT
---

# DXGI_OUTDUPL_MOVE_RECT structure


## -description

The  <b>DXGI_OUTDUPL_MOVE_RECT</b> structure describes the movement of a  rectangle.

## -struct-fields

### -field SourcePoint

The starting position of a rectangle.

### -field DestinationRect

The target region to which to move a rectangle.

## -remarks

This structure is used by <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects">GetFrameMoveRects</a>.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>