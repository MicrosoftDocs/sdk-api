---
UID: NF:d3d10shader.D3D10DisassembleShader
title: D3D10DisassembleShader function (d3d10shader.h)
description: This function -- which disassembles a compiled shader into a text string that contains assembly instructions and register assignments -- has been deprecated. Instead, use D3DDisassemble.
helpviewer_keywords: ["3e4c4f2f-1754-2bbc-636d-9cea485ffad1","D3D10DisassembleShader","D3D10DisassembleShader function [Direct3D 10]","d3d10shader/D3D10DisassembleShader","direct3d10.d3d10disassembleshader"]
old-location: direct3d10\d3d10disassembleshader.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10disassembleshader.htm
ms.date: 12/05/2018
ms.keywords: 3e4c4f2f-1754-2bbc-636d-9cea485ffad1, D3D10DisassembleShader, D3D10DisassembleShader function [Direct3D 10], d3d10shader/D3D10DisassembleShader, direct3d10.d3d10disassembleshader
req.header: d3d10shader.h
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
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10DisassembleShader
 - d3d10shader/D3D10DisassembleShader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D10.dll
api_name:
 - D3D10DisassembleShader
---

# D3D10DisassembleShader function


## -description

This function -- which disassembles a compiled shader into a text string that contains assembly instructions and register assignments -- has been deprecated. Instead, use <a href="/windows/desktop/direct3dhlsl/d3ddisassemble">D3DDisassemble</a>.

## -parameters

### -param pShader [in]

Type: <b>const void*</b>

A pointer to the compiled shader.

### -param BytecodeLength [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

The size of pShader.

### -param EnableColorCode [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Include HTML tags in the output to color code the result.

### -param pComments [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The comment string at the top of the shader that identifies the shader constants and variables.

### -param ppDisassembly [out]

Type: <b><a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob">ID3D10Blob</a>**</b>

Address of a buffer which contains the disassembled shader.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Return value

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-functions">Shader Functions</a>