---
UID: NE:d3dcompiler.D3DCOMPILER_STRIP_FLAGS
title: D3DCOMPILER_STRIP_FLAGS (d3dcompiler.h)
description: Strip flag options.
helpviewer_keywords: ["D3DCOMPILER_STRIP_DEBUG_INFO","D3DCOMPILER_STRIP_FLAGS","D3DCOMPILER_STRIP_FLAGS enumeration [HLSL]","D3DCOMPILER_STRIP_FORCE_DWORD","D3DCOMPILER_STRIP_PRIVATE_DATA","D3DCOMPILER_STRIP_REFLECTION_DATA","D3DCOMPILER_STRIP_ROOT_SIGNATURE","D3DCOMPILER_STRIP_TEST_BLOBS","d2322971-23ee-a7bd-cf13-8a393a03e8a9","d3dcompiler/D3DCOMPILER_STRIP_DEBUG_INFO","d3dcompiler/D3DCOMPILER_STRIP_FLAGS","d3dcompiler/D3DCOMPILER_STRIP_FORCE_DWORD","d3dcompiler/D3DCOMPILER_STRIP_PRIVATE_DATA","d3dcompiler/D3DCOMPILER_STRIP_REFLECTION_DATA","d3dcompiler/D3DCOMPILER_STRIP_ROOT_SIGNATURE","d3dcompiler/D3DCOMPILER_STRIP_TEST_BLOBS","direct3dhlsl.d3dcompiler_strip_flags"]
old-location: direct3dhlsl\d3dcompiler_strip_flags.htm
tech.root: direct3dhlsl
ms.assetid: VS|directx_sdk|~\d3dcompiler_strip_flags.htm
ms.date: 12/05/2018
ms.keywords: D3DCOMPILER_STRIP_DEBUG_INFO, D3DCOMPILER_STRIP_FLAGS, D3DCOMPILER_STRIP_FLAGS enumeration [HLSL], D3DCOMPILER_STRIP_FORCE_DWORD, D3DCOMPILER_STRIP_PRIVATE_DATA, D3DCOMPILER_STRIP_REFLECTION_DATA, D3DCOMPILER_STRIP_ROOT_SIGNATURE, D3DCOMPILER_STRIP_TEST_BLOBS, d2322971-23ee-a7bd-cf13-8a393a03e8a9, d3dcompiler/D3DCOMPILER_STRIP_DEBUG_INFO, d3dcompiler/D3DCOMPILER_STRIP_FLAGS, d3dcompiler/D3DCOMPILER_STRIP_FORCE_DWORD, d3dcompiler/D3DCOMPILER_STRIP_PRIVATE_DATA, d3dcompiler/D3DCOMPILER_STRIP_REFLECTION_DATA, d3dcompiler/D3DCOMPILER_STRIP_ROOT_SIGNATURE, d3dcompiler/D3DCOMPILER_STRIP_TEST_BLOBS, direct3dhlsl.d3dcompiler_strip_flags
req.header: d3dcompiler.h
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
req.typenames: D3DCOMPILER_STRIP_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3DCOMPILER_STRIP_FLAGS
 - d3dcompiler/D3DCOMPILER_STRIP_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3Dcompiler.h
api_name:
 - D3DCOMPILER_STRIP_FLAGS
---

# D3DCOMPILER_STRIP_FLAGS enumeration


## -description

Strip flag options.

## -enum-fields

### -field D3DCOMPILER_STRIP_REFLECTION_DATA:0x00000001

Remove reflection data.

### -field D3DCOMPILER_STRIP_DEBUG_INFO:0x00000002

Remove debug information.

### -field D3DCOMPILER_STRIP_TEST_BLOBS:0x00000004

Remove test blob data.

### -field D3DCOMPILER_STRIP_PRIVATE_DATA:0x00000008

<div class="alert"><b>Note</b>  This value is supported by the D3dcompiler_44.dll or later version of the file.</div>
<div> </div>
Remove private data.

### -field D3DCOMPILER_STRIP_ROOT_SIGNATURE:0x00000010

<div class="alert"><b>Note</b>  This value is supported by the D3dcompiler_47.dll or later version of the file.</div>
<div> </div>
Remove the root signature. Refer to <a href="/windows/desktop/direct3d12/specifying-root-signatures-in-hlsl">Specifying Root Signatures in HLSL</a> for more information on using Direct3D12 with HLSL.

### -field D3DCOMPILER_STRIP_FORCE_DWORD:0x7fffffff

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used.

## -remarks

These flags are used by <a href="/windows/desktop/direct3dhlsl/d3dstripshader">D3DStripShader</a>.

## -see-also

<a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference-enums">Enumerations</a>
