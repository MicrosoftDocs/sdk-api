---
UID: NS:dxgi1_3.DXGI_MATRIX_3X2_F
title: DXGI_MATRIX_3X2_F (dxgi1_3.h)
description: Represents a 3x2 matrix. Used with GetMatrixTransform and SetMatrixTransform to indicate the scaling and translation transform for SwapChainPanel swap chains.
helpviewer_keywords: ["DXGI_MATRIX_3X2_F","DXGI_MATRIX_3X2_F structure [DXGI]","direct3ddxgi.dxgi_matrix_3x2_f","dxgi1_3/DXGI_MATRIX_3X2_F"]
old-location: direct3ddxgi\dxgi_matrix_3x2_f.htm
tech.root: direct3ddxgi
ms.assetid: 5EA0FAD4-5F19-4E5A-97D4-11AE750E8560
ms.date: 12/05/2018
ms.keywords: DXGI_MATRIX_3X2_F, DXGI_MATRIX_3X2_F structure [DXGI], direct3ddxgi.dxgi_matrix_3x2_f, dxgi1_3/DXGI_MATRIX_3X2_F
req.header: dxgi1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
req.typenames: DXGI_MATRIX_3X2_F
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_MATRIX_3X2_F
 - dxgi1_3/DXGI_MATRIX_3X2_F
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgi1_3.h
api_name:
 - DXGI_MATRIX_3X2_F
---

# DXGI_MATRIX_3X2_F structure


## -description

Represents a 3x2 matrix. Used with <a href="/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmatrixtransform">GetMatrixTransform</a> and <a href="/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmatrixtransform">SetMatrixTransform</a> to indicate the scaling and translation transform for <a href="/uwp/api/windows.ui.xaml.controls.swapchainpanel">SwapChainPanel</a> swap chains.

## -struct-fields

### -field _11

The value in the first row and first column of the matrix.

### -field _12

The value in the first row and second column of the matrix.

### -field _21

The value in the second row and first column of the matrix.

### -field _22

The value in the second row and second column of the matrix.

### -field _31

The value in the third row and first column of the matrix.

### -field _32

The value in the third row and second column of the matrix.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>