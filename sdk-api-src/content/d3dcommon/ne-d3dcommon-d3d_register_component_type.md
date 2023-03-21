---
UID: NE:d3dcommon.D3D_REGISTER_COMPONENT_TYPE
title: D3D_REGISTER_COMPONENT_TYPE (d3dcommon.h)
description: Values that identify the data types that can be stored in a register.
helpviewer_keywords: ["D3D10_REGISTER_COMPONENT_FLOAT32","D3D10_REGISTER_COMPONENT_SINT32","D3D10_REGISTER_COMPONENT_UINT32","D3D10_REGISTER_COMPONENT_UNKNOWN","D3D_REGISTER_COMPONENT_FLOAT32","D3D_REGISTER_COMPONENT_SINT32","D3D_REGISTER_COMPONENT_TYPE","D3D_REGISTER_COMPONENT_TYPE enumeration [Direct3D 11]","D3D_REGISTER_COMPONENT_UINT32","D3D_REGISTER_COMPONENT_UNKNOWN","d3dcommon/D3D10_REGISTER_COMPONENT_FLOAT32","d3dcommon/D3D10_REGISTER_COMPONENT_SINT32","d3dcommon/D3D10_REGISTER_COMPONENT_UINT32","d3dcommon/D3D10_REGISTER_COMPONENT_UNKNOWN","d3dcommon/D3D_REGISTER_COMPONENT_FLOAT32","d3dcommon/D3D_REGISTER_COMPONENT_SINT32","d3dcommon/D3D_REGISTER_COMPONENT_TYPE","d3dcommon/D3D_REGISTER_COMPONENT_UINT32","d3dcommon/D3D_REGISTER_COMPONENT_UNKNOWN","direct3d11.d3d_register_component_type"]
old-location: direct3d11\d3d_register_component_type.htm
tech.root: direct3d11
ms.assetid: 71e3c707-745b-40b4-ba3c-6c501196e3d3
ms.date: 12/05/2018
ms.keywords: D3D10_REGISTER_COMPONENT_FLOAT32, D3D10_REGISTER_COMPONENT_SINT32, D3D10_REGISTER_COMPONENT_UINT32, D3D10_REGISTER_COMPONENT_UNKNOWN, D3D_REGISTER_COMPONENT_FLOAT32, D3D_REGISTER_COMPONENT_SINT32, D3D_REGISTER_COMPONENT_TYPE, D3D_REGISTER_COMPONENT_TYPE enumeration [Direct3D 11], D3D_REGISTER_COMPONENT_UINT32, D3D_REGISTER_COMPONENT_UNKNOWN, d3dcommon/D3D10_REGISTER_COMPONENT_FLOAT32, d3dcommon/D3D10_REGISTER_COMPONENT_SINT32, d3dcommon/D3D10_REGISTER_COMPONENT_UINT32, d3dcommon/D3D10_REGISTER_COMPONENT_UNKNOWN, d3dcommon/D3D_REGISTER_COMPONENT_FLOAT32, d3dcommon/D3D_REGISTER_COMPONENT_SINT32, d3dcommon/D3D_REGISTER_COMPONENT_TYPE, d3dcommon/D3D_REGISTER_COMPONENT_UINT32, d3dcommon/D3D_REGISTER_COMPONENT_UNKNOWN, direct3d11.d3d_register_component_type
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
req.typenames: D3D_REGISTER_COMPONENT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D_REGISTER_COMPONENT_TYPE
 - d3dcommon/D3D_REGISTER_COMPONENT_TYPE
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
 - D3D_REGISTER_COMPONENT_TYPE
---

# D3D_REGISTER_COMPONENT_TYPE enumeration


## -description

Values that identify the data types that can be stored in a register.

> [!NOTE]
> For programming with Direct3D 10, this API has a type alias that begins `D3D10_` instead of `D3D_`. These Direct3D 10 type aliases are defined in `d3d10.h`, `d3d10misc.h`, and `d3d10shader.h`.

## -enum-fields

### -field D3D_REGISTER_COMPONENT_UNKNOWN:0

The data type is unknown.

### -field D3D_REGISTER_COMPONENT_UINT32:1

32-bit unsigned integer.

### -field D3D_REGISTER_COMPONENT_SINT32:2

32-bit signed integer.

### -field D3D_REGISTER_COMPONENT_FLOAT32:3

32-bit floating-point number.

### -field D3D10_REGISTER_COMPONENT_UNKNOWN

The data type is unknown.

### -field D3D10_REGISTER_COMPONENT_UINT32

32-bit unsigned integer.

### -field D3D10_REGISTER_COMPONENT_SINT32

32-bit signed integer.

### -field D3D10_REGISTER_COMPONENT_FLOAT32

32-bit floating-point number.

## -remarks

A register component type is specified in the <b>ComponentType</b> member of the <a href="/windows/win32/api/d3d11shader/ns-d3d11shader-d3d11_signature_parameter_desc">D3D11_SIGNATURE_PARAMETER_DESC</a> structure.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-common-enumerations">Common Version Enumerations</a>
