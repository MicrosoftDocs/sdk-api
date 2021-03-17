---
UID: NS:dxgi1_2.DXGI_OUTDUPL_POINTER_POSITION
title: DXGI_OUTDUPL_POINTER_POSITION (dxgi1_2.h)
description: The DXGI_OUTDUPL_POINTER_POSITION structure describes the position of the hardware cursor.
helpviewer_keywords: ["DXGI_OUTDUPL_POINTER_POSITION","DXGI_OUTDUPL_POINTER_POSITION structure [DXGI]","direct3ddxgi.dxgi_outdupl_pointer_position","dxgi1_2/DXGI_OUTDUPL_POINTER_POSITION"]
old-location: direct3ddxgi\dxgi_outdupl_pointer_position.htm
tech.root: direct3ddxgi
ms.assetid: CCD55021-8F67-463D-BA00-46D8B9D22B9A
ms.date: 12/05/2018
ms.keywords: DXGI_OUTDUPL_POINTER_POSITION, DXGI_OUTDUPL_POINTER_POSITION structure [DXGI], direct3ddxgi.dxgi_outdupl_pointer_position, dxgi1_2/DXGI_OUTDUPL_POINTER_POSITION
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
req.typenames: DXGI_OUTDUPL_POINTER_POSITION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_OUTDUPL_POINTER_POSITION
 - dxgi1_2/DXGI_OUTDUPL_POINTER_POSITION
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
 - DXGI_OUTDUPL_POINTER_POSITION
---

# DXGI_OUTDUPL_POINTER_POSITION structure


## -description

The <b>DXGI_OUTDUPL_POINTER_POSITION</b> structure describes the position of the hardware cursor.

## -struct-fields

### -field Position

The position of the hardware cursor relative to the top-left of the adapter output.

### -field Visible

Specifies whether the hardware cursor is visible. <b>TRUE</b> if visible; otherwise, <b>FALSE</b>. If the hardware cursor is not visible, the calling application does not display the cursor in the client.

## -remarks

The <b>Position</b> member is valid only if the <b>Visible</b> member’s value is set to <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>



<a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_outdupl_frame_info">DXGI_OUTDUPL_FRAME_INFO</a>