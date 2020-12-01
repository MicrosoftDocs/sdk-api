---
UID: NS:ddraw._DDOVERLAYFX
title: DDOVERLAYFX (ddraw.h)
description: The DDOVERLAYFX structure passes overlay information to the IDirectDrawSurface7::UpdateOverlay method.
helpviewer_keywords: ["*LPDDOVERLAYFX","DDOVERFX_ARITHSTRETCHY","DDOVERFX_MIRRORLEFTRIGHT","DDOVERFX_MIRRORUPDOWN","DDOVERLAYFX","DDOVERLAYFX structure [DirectDraw]","LPDDOVERLAYFX","LPDDOVERLAYFX structure pointer [DirectDraw]","ddraw/DDOVERLAYFX","ddraw/LPDDOVERLAYFX","directdraw.ddoverlayfx"]
old-location: directdraw\ddoverlayfx.htm
tech.root: directdraw
ms.assetid: 83b56211-0483-4e22-90b4-83ac5eaaa2f4
ms.date: 12/05/2018
ms.keywords: '*LPDDOVERLAYFX, DDOVERFX_ARITHSTRETCHY, DDOVERFX_MIRRORLEFTRIGHT, DDOVERFX_MIRRORUPDOWN, DDOVERLAYFX, DDOVERLAYFX structure [DirectDraw], LPDDOVERLAYFX, LPDDOVERLAYFX structure pointer [DirectDraw], ddraw/DDOVERLAYFX, ddraw/LPDDOVERLAYFX, directdraw.ddoverlayfx'
req.header: ddraw.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DDOVERLAYFX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDOVERLAYFX
 - ddraw/_DDOVERLAYFX
 - DDOVERLAYFX
 - ddraw/DDOVERLAYFX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ddraw.h
api_name:
 - DDOVERLAYFX
---

## -description

The <b>DDOVERLAYFX</b> structure passes overlay information to the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay">IDirectDrawSurface7::UpdateOverlay</a> method.

## -struct-fields

### -field dwSize

Size of the structure, in bytes. This member must be initialized before the structure is used.

### -field dwAlphaEdgeBlendBitDepth

Bit depth used to specify the constant for an alpha edge blend.

### -field dwAlphaEdgeBlend

Constant to use as the alpha for an edge blend.

### -field dwReserved

Reserved

### -field dwAlphaDestConstBitDepth

Bit depth used to specify the alpha constant for a destination.

### -field DUMMYUNIONNAMEN.dwAlphaDestConst

Constant to use as the alpha channel for a destination.

### -field DUMMYUNIONNAMEN.lpDDSAlphaDest

Address of a surface to use as the alpha channel for a destination.

### -field dwAlphaSrcConstBitDepth

Bit depth used to specify the alpha constant for a source.

### -field DUMMYUNIONNAMEN

See **Remarks**.

### -field DUMMYUNIONNAMEN.dwAlphaSrcConst

Constant to use as the alpha channel for a source.

### -field DUMMYUNIONNAMEN.lpDDSAlphaSrc

Address of a surface to use as the alpha channel for a source.

### -field dckDestColorkey

Destination color key for the overlay.

### -field dckSrcColorkey

Source color key for the overlay.

### -field dwDDFX

The following flags that specify overlay effects.

#### DDOVERFX_ARITHSTRETCHY

If stretching, use arithmetic stretching along the y-axis for this overlay.

#### DDOVERFX_MIRRORLEFTRIGHT

Mirror the overlay around the vertical axis.

#### DDOVERFX_MIRRORUPDOWN

Mirror the overlay around the horizontal axis.

### -field dwFlags

Currently not used and must be set to 0.

## -remarks

The unions in this structure have been updated to work with compilers that do not support nameless unions. If your compiler does not support nameless unions, define the NONAMELESSUNION token before including the Ddraw.h header file.