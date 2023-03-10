---
UID: NE:d3dcommon._D3D_CBUFFER_TYPE
title: D3D_CBUFFER_TYPE (d3dcommon.h)
description: Values that identify the intended use of constant-buffer data.
helpviewer_keywords: ["D3D10_CT_CBUFFER","D3D10_CT_TBUFFER","D3D11_CT_CBUFFER","D3D11_CT_INTERFACE_POINTERS","D3D11_CT_RESOURCE_BIND_INFO","D3D11_CT_TBUFFER","D3D_CBUFFER_TYPE","D3D_CBUFFER_TYPE enumeration [Direct3D 11]","D3D_CT_CBUFFER","D3D_CT_INTERFACE_POINTERS","D3D_CT_RESOURCE_BIND_INFO","D3D_CT_TBUFFER","d3dcommon/D3D10_CT_CBUFFER","d3dcommon/D3D10_CT_TBUFFER","d3dcommon/D3D11_CT_CBUFFER","d3dcommon/D3D11_CT_INTERFACE_POINTERS","d3dcommon/D3D11_CT_RESOURCE_BIND_INFO","d3dcommon/D3D11_CT_TBUFFER","d3dcommon/D3D_CBUFFER_TYPE","d3dcommon/D3D_CT_CBUFFER","d3dcommon/D3D_CT_INTERFACE_POINTERS","d3dcommon/D3D_CT_RESOURCE_BIND_INFO","d3dcommon/D3D_CT_TBUFFER","direct3d11.d3d_cbuffer_type"]
old-location: direct3d11\d3d_cbuffer_type.htm
tech.root: direct3d11
ms.assetid: b21a460b-63cb-49c1-bd6c-a747df495efc
ms.date: 12/05/2018
ms.keywords: D3D10_CT_CBUFFER, D3D10_CT_TBUFFER, D3D11_CT_CBUFFER, D3D11_CT_INTERFACE_POINTERS, D3D11_CT_RESOURCE_BIND_INFO, D3D11_CT_TBUFFER, D3D_CBUFFER_TYPE, D3D_CBUFFER_TYPE enumeration [Direct3D 11], D3D_CT_CBUFFER, D3D_CT_INTERFACE_POINTERS, D3D_CT_RESOURCE_BIND_INFO, D3D_CT_TBUFFER, d3dcommon/D3D10_CT_CBUFFER, d3dcommon/D3D10_CT_TBUFFER, d3dcommon/D3D11_CT_CBUFFER, d3dcommon/D3D11_CT_INTERFACE_POINTERS, d3dcommon/D3D11_CT_RESOURCE_BIND_INFO, d3dcommon/D3D11_CT_TBUFFER, d3dcommon/D3D_CBUFFER_TYPE, d3dcommon/D3D_CT_CBUFFER, d3dcommon/D3D_CT_INTERFACE_POINTERS, d3dcommon/D3D_CT_RESOURCE_BIND_INFO, d3dcommon/D3D_CT_TBUFFER, direct3d11.d3d_cbuffer_type
req.header: d3dcommon.h
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
req.typenames: D3D_CBUFFER_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D_CBUFFER_TYPE
 - d3dcommon/_D3D_CBUFFER_TYPE
 - D3D_CBUFFER_TYPE
 - d3dcommon/D3D_CBUFFER_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3DCommon.h
api_name:
 - D3D_CBUFFER_TYPE
---

## -description

Values that identify the intended use of constant-buffer data. 

> [!NOTE]
> For programming with Direct3D 10, this API has a type alias that begins `D3D10_` instead of `D3D_`. These Direct3D 10 type aliases are defined in `d3d10.h`, `d3d10misc.h`, and `d3d10shader.h`.

## -enum-fields

### -field D3D_CT_CBUFFER:0

A buffer containing scalar constants.

### -field D3D_CT_TBUFFER

A buffer containing texture data.

### -field D3D_CT_INTERFACE_POINTERS

A buffer containing interface pointers.

### -field D3D_CT_RESOURCE_BIND_INFO

A buffer containing binding information.

### -field D3D10_CT_CBUFFER

A buffer containing scalar constants.

### -field D3D10_CT_TBUFFER

A buffer containing texture data.

### -field D3D11_CT_CBUFFER

A buffer containing scalar constants.

### -field D3D11_CT_TBUFFER

A buffer containing texture data.

### -field D3D11_CT_INTERFACE_POINTERS

A buffer containing interface pointers.

### -field D3D11_CT_RESOURCE_BIND_INFO

A buffer containing binding information.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-common-enumerations">Common Version Enumerations</a>
