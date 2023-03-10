---
UID: NF:d3d10shader.D3D10GetInputAndOutputSignatureBlob
title: D3D10GetInputAndOutputSignatureBlob function (d3d10shader.h)
description: Get a buffer that contains shader signatures.
helpviewer_keywords: ["D3D10GetInputAndOutputSignatureBlob","D3D10GetInputAndOutputSignatureBlob function [Direct3D 10]","d3d10shader/D3D10GetInputAndOutputSignatureBlob","direct3d10.d3d10getinputandoutputsignatureblob","f10e041a-6f66-0e2b-400e-a60c10b92deb"]
old-location: direct3d10\d3d10getinputandoutputsignatureblob.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10getinputandoutputsignatureblob.htm
ms.date: 12/05/2018
ms.keywords: D3D10GetInputAndOutputSignatureBlob, D3D10GetInputAndOutputSignatureBlob function [Direct3D 10], d3d10shader/D3D10GetInputAndOutputSignatureBlob, direct3d10.d3d10getinputandoutputsignatureblob, f10e041a-6f66-0e2b-400e-a60c10b92deb
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
 - D3D10GetInputAndOutputSignatureBlob
 - d3d10shader/D3D10GetInputAndOutputSignatureBlob
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
 - D3D10GetInputAndOutputSignatureBlob
---

# D3D10GetInputAndOutputSignatureBlob function


## -description

Get a buffer that contains shader signatures.

## -parameters

### -param pShaderBytecode [in]

Type: <b>const void*</b>

A pointer to the compiled shader. To get this pointer see <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10">Getting a Pointer to a Compiled Shader</a>.

### -param BytecodeLength [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

The size of the shader bytecode in bytes.

### -param ppSignatureBlob [out]

Type: <b><a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob">ID3D10Blob</a>**</b>

The address of a pointer to the buffer (see <a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob">ID3D10Blob Interface</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-functions">Core Functions</a>



<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-functions">Shader Functions</a>