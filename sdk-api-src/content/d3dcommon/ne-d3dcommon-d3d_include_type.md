---
UID: NE:d3dcommon._D3D_INCLUDE_TYPE
title: D3D_INCLUDE_TYPE (d3dcommon.h)
description: Values that indicate the location of a shader
helpviewer_keywords: ["D3D10_INCLUDE_LOCAL","D3D10_INCLUDE_SYSTEM","D3D_INCLUDE_FORCE_DWORD","D3D_INCLUDE_LOCAL","D3D_INCLUDE_SYSTEM","D3D_INCLUDE_TYPE","D3D_INCLUDE_TYPE enumeration [Direct3D 11]","d3dcommon/D3D10_INCLUDE_LOCAL","d3dcommon/D3D10_INCLUDE_SYSTEM","d3dcommon/D3D_INCLUDE_FORCE_DWORD","d3dcommon/D3D_INCLUDE_LOCAL","d3dcommon/D3D_INCLUDE_SYSTEM","d3dcommon/D3D_INCLUDE_TYPE","direct3d11.d3d_include_type"]
old-location: direct3d11\d3d_include_type.htm
tech.root: direct3d11
ms.assetid: 98f0b0dd-9ff8-4321-a9ea-2deabc9529f2
ms.date: 12/05/2018
ms.keywords: D3D10_INCLUDE_LOCAL, D3D10_INCLUDE_SYSTEM, D3D_INCLUDE_FORCE_DWORD, D3D_INCLUDE_LOCAL, D3D_INCLUDE_SYSTEM, D3D_INCLUDE_TYPE, D3D_INCLUDE_TYPE enumeration [Direct3D 11], d3dcommon/D3D10_INCLUDE_LOCAL, d3dcommon/D3D10_INCLUDE_SYSTEM, d3dcommon/D3D_INCLUDE_FORCE_DWORD, d3dcommon/D3D_INCLUDE_LOCAL, d3dcommon/D3D_INCLUDE_SYSTEM, d3dcommon/D3D_INCLUDE_TYPE, direct3d11.d3d_include_type
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
req.typenames: D3D_INCLUDE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D_INCLUDE_TYPE
 - d3dcommon/_D3D_INCLUDE_TYPE
 - D3D_INCLUDE_TYPE
 - d3dcommon/D3D_INCLUDE_TYPE
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
 - D3D_INCLUDE_TYPE
---

# D3D_INCLUDE_TYPE enumeration


## -description

Values that indicate the location of a shader #include file. 

> [!NOTE]
> For programming with Direct3D 10, this API has a type alias that begins `D3D10_` instead of `D3D_`. These Direct3D 10 type aliases are defined in `d3d10.h`, `d3d10misc.h`, and `d3d10shader.h`.

## -enum-fields

### -field D3D_INCLUDE_LOCAL:0

The local directory.

### -field D3D_INCLUDE_SYSTEM

The system directory.

### -field D3D10_INCLUDE_LOCAL

The local directory.

### -field D3D10_INCLUDE_SYSTEM

The system directory.

### -field D3D_INCLUDE_FORCE_DWORD:0x7fffffff

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. 

Do not use this value.

## -remarks

You pass a <b>D3D_INCLUDE_TYPE</b>-typed value to the  <i>IncludeType</i> parameter in a call to the  <a href="/windows/desktop/api/d3dcommon/nf-d3dcommon-id3dinclude-open">ID3DInclude::Open</a> method to indicate the location of the #include file.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-common-enumerations">Common Version Enumerations</a>



<a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_include_type">D3D_INCLUDE_TYPE</a>



<a href="/windows/desktop/api/d3dcommon/nf-d3dcommon-id3dinclude-open">ID3DInclude::Open</a>
