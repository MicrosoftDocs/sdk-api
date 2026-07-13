---
UID: NF:d3d10.ID3D10Device.CreateGeometryShaderWithStreamOutput
title: ID3D10Device::CreateGeometryShaderWithStreamOutput (d3d10.h)
description: Creates a geometry shader that can write to streaming output buffers. (ID3D10Device.CreateGeometryShaderWithStreamOutput)
helpviewer_keywords: ["1ef110f5-f95f-ec17-1f56-6f491a0ffac4","CreateGeometryShaderWithStreamOutput","CreateGeometryShaderWithStreamOutput method [Direct3D 10]","CreateGeometryShaderWithStreamOutput method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","CreateGeometryShaderWithStreamOutput method","ID3D10Device.CreateGeometryShaderWithStreamOutput","ID3D10Device::CreateGeometryShaderWithStreamOutput","d3d10/ID3D10Device::CreateGeometryShaderWithStreamOutput","direct3d10.id3d10device_creategeometryshaderwithstreamoutput"]
old-location: direct3d10\id3d10device_creategeometryshaderwithstreamoutput.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_creategeometryshaderwithstreamoutput.htm
ms.date: 12/05/2018
ms.keywords: 1ef110f5-f95f-ec17-1f56-6f491a0ffac4, CreateGeometryShaderWithStreamOutput, CreateGeometryShaderWithStreamOutput method [Direct3D 10], CreateGeometryShaderWithStreamOutput method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateGeometryShaderWithStreamOutput method, ID3D10Device.CreateGeometryShaderWithStreamOutput, ID3D10Device::CreateGeometryShaderWithStreamOutput, d3d10/ID3D10Device::CreateGeometryShaderWithStreamOutput, direct3d10.id3d10device_creategeometryshaderwithstreamoutput
req.header: d3d10.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Device::CreateGeometryShaderWithStreamOutput
 - d3d10/ID3D10Device::CreateGeometryShaderWithStreamOutput
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.CreateGeometryShaderWithStreamOutput
---

# ID3D10Device::CreateGeometryShaderWithStreamOutput


## -description

Creates a geometry shader that can write to streaming output buffers.

## -parameters

### -param pShaderBytecode [in]

Type: <b>const void*</b>

A pointer to the compiled geometry shader for a standard geometry shader plus stream output. For info on how to get this pointer, see <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10">Getting a Pointer to a Compiled Shader</a>.

To create the stream output without using a geometry shader, pass a pointer to the output signature for the prior stage. To obtain this output signature, call the <a href="/windows/desktop/direct3dhlsl/d3dgetoutputsignatureblob">D3DGetOutputSignatureBlob</a> compiler function. You can also pass a pointer to the compiled <a href="/previous-versions/bb205146(v=vs.85)">vertex shader</a> that is used in the prior stage. This compiled shader provides the output signature for the data.

### -param BytecodeLength [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

Size of the compiled geometry shader.

### -param pSODeclaration [in]

Type: <b>const <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_so_declaration_entry">D3D10_SO_DECLARATION_ENTRY</a>*</b>

Pointer to a <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_so_declaration_entry">D3D10_SO_DECLARATION_ENTRY</a> array. Cannot be <b>NULL</b> if <i>NumEntries</i>&gt; 0.

### -param NumEntries [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of entries in the array pointed to by <i>pSODeclaration</i>. Minimum 0, maximum 64.

### -param OutputStreamStride [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The size, in bytes, of each element in the array pointed to by <i>pSODeclaration</i>. This parameter is only used when the output slot is 0 for all entries in <i>pSODeclaration</i>.

### -param ppGeometryShader [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10geometryshader">ID3D10GeometryShader</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10geometryshader">ID3D10GeometryShader Interface</a>. If this is <b>NULL</b>, all other parameters will be validated, and if all parameters pass validation this API will return S_FALSE instead of S_OK.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

For more info about using <b>CreateGeometryShaderWithStreamOutput</b>, see <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage-getting-started">Create a Geometry-Shader Object with Stream Output</a>.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
