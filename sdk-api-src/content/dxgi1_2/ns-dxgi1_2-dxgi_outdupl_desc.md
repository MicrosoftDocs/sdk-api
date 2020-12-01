---
UID: NS:dxgi1_2.DXGI_OUTDUPL_DESC
title: DXGI_OUTDUPL_DESC (dxgi1_2.h)
description: The DXGI_OUTDUPL_DESC structure describes the dimension of the output and the surface that contains the desktop image. The format of the desktop image is always DXGI_FORMAT_B8G8R8A8_UNORM.
helpviewer_keywords: ["DXGI_OUTDUPL_DESC","DXGI_OUTDUPL_DESC structure [DXGI]","direct3ddxgi.dxgi_outdupl_desc","dxgi1_2/DXGI_OUTDUPL_DESC"]
old-location: direct3ddxgi\dxgi_outdupl_desc.htm
tech.root: direct3ddxgi
ms.assetid: 003014E3-4322-4253-8D69-AE315CDFDA75
ms.date: 12/05/2018
ms.keywords: DXGI_OUTDUPL_DESC, DXGI_OUTDUPL_DESC structure [DXGI], direct3ddxgi.dxgi_outdupl_desc, dxgi1_2/DXGI_OUTDUPL_DESC
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
req.typenames: DXGI_OUTDUPL_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_OUTDUPL_DESC
 - dxgi1_2/DXGI_OUTDUPL_DESC
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
 - DXGI_OUTDUPL_DESC
---

# DXGI_OUTDUPL_DESC structure


## -description

The DXGI_OUTDUPL_DESC structure describes the dimension of the output and the surface that contains the desktop image. The format of the desktop image is always <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_B8G8R8A8_UNORM</a>.

## -struct-fields

### -field ModeDesc

A <a href="/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)">DXGI_MODE_DESC</a> structure that describes the display mode of the duplicated output.

### -field Rotation

A member of the <a href="/previous-versions/windows/desktop/legacy/bb173065(v=vs.85)">DXGI_MODE_ROTATION</a> enumerated type that describes how the duplicated output rotates an image.

### -field DesktopImageInSystemMemory

Specifies whether the resource that contains the desktop image is already located in system memory. <b>TRUE</b> if the resource is in system memory; otherwise, <b>FALSE</b>. If this value is <b>TRUE</b> and  the application requires CPU access, it can use the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutputduplication-mapdesktopsurface">IDXGIOutputDuplication::MapDesktopSurface</a> and <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutputduplication-unmapdesktopsurface">IDXGIOutputDuplication::UnMapDesktopSurface</a> methods to avoid copying the data into a staging buffer.

## -remarks

This structure is used by <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutputduplication-getdesc">GetDesc</a>.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>