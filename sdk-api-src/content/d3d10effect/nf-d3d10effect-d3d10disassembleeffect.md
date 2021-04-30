---
UID: NF:d3d10effect.D3D10DisassembleEffect
title: D3D10DisassembleEffect function (d3d10effect.h)
description: This function -- which disassembles a compiled effect into a text string that contains assembly instructions and register assignments -- has been deprecated. Instead, use D3DDisassemble10Effect.
helpviewer_keywords: ["10ff0da2-3f88-22ec-7841-61c27051dfa6","D3D10DisassembleEffect","D3D10DisassembleEffect function [Direct3D 10]","d3d10effect/D3D10DisassembleEffect","direct3d10.d3d10disassembleeffect"]
old-location: direct3d10\d3d10disassembleeffect.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10disassembleeffect.htm
ms.date: 12/05/2018
ms.keywords: 10ff0da2-3f88-22ec-7841-61c27051dfa6, D3D10DisassembleEffect, D3D10DisassembleEffect function [Direct3D 10], d3d10effect/D3D10DisassembleEffect, direct3d10.d3d10disassembleeffect
req.header: d3d10effect.h
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
 - D3D10DisassembleEffect
 - d3d10effect/D3D10DisassembleEffect
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
 - D3D10DisassembleEffect
---

# D3D10DisassembleEffect function


## -description

This function -- which disassembles a compiled effect into a text string that contains assembly instructions and register assignments -- has been deprecated. Instead, use <a href="/windows/desktop/direct3dhlsl/d3ddisassemble10effect">D3DDisassemble10Effect</a>.

## -parameters

### -param pEffect [in]

Type: <b><a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect">ID3D10Effect</a>*</b>

A pointer to an <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect">ID3D10Effect Interface</a>, which contains the compiled effect.

### -param EnableColorCode [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Include HTML tags in the output to color code the result.

### -param ppDisassembly [out]

Type: <b><a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob">ID3D10Blob</a>**</b>

A pointer to an <a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob">ID3D10Blob Interface</a> which contains the disassembled shader.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

This returned text includes a header with the version of the HLSL compiler used to generate this object, comments describing the memory layout of the constant buffers used by the shader, input and output signatures, and resource binding points.

Here is an example of disassembling a compiled effect. The example assumes you start with a compiled effect (shown as <i>l_pBlob_Effect</i> which you can see in <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-effects-compile">Compile an Effect (Direct3D 10)</a>).


```

LPCSTR commentString = NULL;
ID3D10Blob* pIDisassembly = NULL;
char* pDisassembly = NULL;
if( pVSBuf )
{
    D3D10DisassembleEffect( (UINT*) l_pBlob_Effect->GetBufferPointer(),
        l_pBlob_Effect->GetBufferSize(), TRUE, commentString, &pIDisassembly );
    if( pIDisassembly )
    {
        FILE* pFile = fopen( "effect.htm", "w" );
        if( pFile)
        {
            fputs( (char*)pIDisassembly->GetBufferPointer(), pFile );
            fclose( pFile );
        }
    }
}

```

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-effect-functions">Effect Functions (Direct3D 10)</a>