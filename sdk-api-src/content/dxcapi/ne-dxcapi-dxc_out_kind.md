---
UID: NE:dxcapi.DXC_OUT_KIND
tech.root: direct3dhlsl
title: DXC_OUT_KIND
ms.date: 04/05/2023
targetos: Windows
description: Specifies the kind of output to retrieve from an [IDxcResult](./ns-dxcapi-idxcresult.md).
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: dxcapi.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
typedef_isUnnamed: false
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - dxcapi.h
api_name:
 - DXC_OUT_KIND
f1_keywords:
 - DXC_OUT_KIND
 - dxcapi/DXC_OUT_KIND
dev_langs:
 - c++
helpviewer_keywords:
 - DXC_OUT_KIND
---

## -description

Defines constants that specify the kind of output to retrieve from an [IDxcResult](./ns-dxcapi-idxcresult.md). For use with the *dxcOutKind* parameter of [IDxcResult::GetOutput](./nf-dxcapi-idxcresult-getoutput.md) and [IDxcResult::HasOutput](./nf-dxcapi-idxcresult-hasoutput).

> [!NOTE]
> Text outputs returned from version 2 APIs are UTF-8 or UTF-16, depending on the `-encoding` option passed to the compiler.

## -enum-fields

### -field DXC_OUT_NONE:0

Specifies no output.

### -field DXC_OUT_OBJECT:1

For [IDxcBlob](./ns-dxcapi-idxcblob), specifies a shader or library object.

### -field DXC_OUT_ERRORS:2

For [IDxcBlobUtf8](./ns-dxcapi-idxcblobutf8) or [IDxcBlobUtf16](./ns-dxcapi-idxcblobutf16), specifies errors.

### -field DXC_OUT_PDB:3

For [IDxcBlob](./ns-dxcapi-idxcblob), specifies PDB.

### -field DXC_OUT_SHADER_HASH:4

For [IDxcBlob](./ns-dxcapi-idxcblob), specifies the DxcShaderHash of a shader or a shader with source info (`-Zsb/-Zss`).

### -field DXC_OUT_DISASSEMBLY:5

For [IDxcBlobUtf8](./ns-dxcapi-idxcblobutf8) or [IDxcBlobUtf16](./ns-dxcapi-idxcblobutf16), specifies the output from disassembling.

### -field DXC_OUT_HLSL:6

For [IDxcBlobUtf8](./ns-dxcapi-idxcblobutf8) or [IDxcBlobUtf16](./ns-dxcapi-idxcblobutf16), specifies the output from the preprocessor or rewriter.

### -field DXC_OUT_TEXT:7

For [IDxcBlobUtf8](./ns-dxcapi-idxcblobutf8) or [IDxcBlobUtf16](./ns-dxcapi-idxcblobutf16), specifies other text, such as `-ast-dump` or `-Odump`.

### -field DXC_OUT_REFLECTION:8

For [IDxcBlob](./ns-dxcapi-idxcblob), specifies the RDAT part with reflection data.

### -field DXC_OUT_ROOT_SIGNATURE:9

For [IDxcBlob](./ns-dxcapi-idxcblob), specifies serialized root signature output.

### -field DXC_OUT_EXTRA_OUTPUTS:10

For [IDxcExtraOutputs](./ns-dxcapi-idxcextraoutputs), specifies extra outputs.

### -field DXC_OUT_FORCE_DWORD:0xFFFFFFFF

## -remarks

## -see-also
