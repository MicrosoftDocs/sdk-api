---
UID: NF:d3d11.ID3D11Device.CreateGeometryShaderWithStreamOutput
title: ID3D11Device::CreateGeometryShaderWithStreamOutput (d3d11.h)
description: Creates a geometry shader that can write to streaming output buffers. (ID3D11Device.CreateGeometryShaderWithStreamOutput)
helpviewer_keywords: ["39026c1a-ac13-562f-6f6e-86f1981ebb87","CreateGeometryShaderWithStreamOutput","CreateGeometryShaderWithStreamOutput method [Direct3D 11]","CreateGeometryShaderWithStreamOutput method [Direct3D 11]","ID3D11Device interface","ID3D11Device interface [Direct3D 11]","CreateGeometryShaderWithStreamOutput method","ID3D11Device.CreateGeometryShaderWithStreamOutput","ID3D11Device::CreateGeometryShaderWithStreamOutput","d3d11/ID3D11Device::CreateGeometryShaderWithStreamOutput","direct3d11.id3d11device_creategeometryshaderwithstreamoutput"]
old-location: direct3d11\id3d11device_creategeometryshaderwithstreamoutput.htm
tech.root: direct3d11
ms.assetid: 69499121-6f35-4cf1-b115-9ffdce26e4b0
ms.date: 12/05/2018
ms.keywords: 39026c1a-ac13-562f-6f6e-86f1981ebb87, CreateGeometryShaderWithStreamOutput, CreateGeometryShaderWithStreamOutput method [Direct3D 11], CreateGeometryShaderWithStreamOutput method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateGeometryShaderWithStreamOutput method, ID3D11Device.CreateGeometryShaderWithStreamOutput, ID3D11Device::CreateGeometryShaderWithStreamOutput, d3d11/ID3D11Device::CreateGeometryShaderWithStreamOutput, direct3d11.id3d11device_creategeometryshaderwithstreamoutput
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Device::CreateGeometryShaderWithStreamOutput
 - d3d11/ID3D11Device::CreateGeometryShaderWithStreamOutput
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device.CreateGeometryShaderWithStreamOutput
---

# ID3D11Device::CreateGeometryShaderWithStreamOutput


## -description

Creates a geometry shader that can write to streaming output buffers.

## -parameters

### -param pShaderBytecode [in]

Type: <b>const void*</b>

A pointer to the compiled geometry shader for a standard geometry shader plus stream output. For info on how to get this pointer, see <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10">Getting a Pointer to a Compiled Shader</a>.

To create the stream output without using a geometry shader, pass a pointer to the output signature for the prior stage. To obtain this output signature, call the <a href="/windows/desktop/direct3dhlsl/d3dgetoutputsignatureblob">D3DGetOutputSignatureBlob</a> compiler function. You can also pass a pointer to the compiled shader for the prior stage (for example, the <a href="/previous-versions/bb205146(v=vs.85)">vertex-shader stage</a> or <a href="/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation">domain-shader stage</a>). This compiled shader provides the output signature for the data.

### -param BytecodeLength [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

Size of the compiled geometry shader.

### -param pSODeclaration [in, optional]

Type: <b>const <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_so_declaration_entry">D3D11_SO_DECLARATION_ENTRY</a>*</b>

Pointer to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_so_declaration_entry">D3D11_SO_DECLARATION_ENTRY</a> array. Cannot be <b>NULL</b> if NumEntries &gt; 0.

### -param NumEntries [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of entries in the stream output declaration ( ranges from 0 to D3D11_SO_STREAM_COUNT * D3D11_SO_OUTPUT_COMPONENT_COUNT ).

### -param pBufferStrides [in, optional]

Type: <b>const <a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

An array of buffer strides; each stride is the size of an element for that buffer.

### -param NumStrides [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of strides (or buffers) in <i>pBufferStrides</i> (ranges from 0 to D3D11_SO_BUFFER_SLOT_COUNT).

### -param RasterizedStream [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index number of the stream to be sent to the rasterizer stage (ranges from 0 to D3D11_SO_STREAM_COUNT - 1).
              Set to D3D11_SO_NO_RASTERIZED_STREAM if no stream is to be rasterized.

### -param pClassLinkage [in, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classlinkage">ID3D11ClassLinkage</a>*</b>

A pointer to a class linkage interface (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classlinkage">ID3D11ClassLinkage</a>); the value can be <b>NULL</b>.

### -param ppGeometryShader [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader">ID3D11GeometryShader</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader">ID3D11GeometryShader</a> interface, representing the geometry shader that was created.
            Set this to <b>NULL</b> to validate the other parameters; if validation passes, the method will return S_FALSE instead of S_OK.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

For more info about using <b>CreateGeometryShaderWithStreamOutput</b>, see <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage-getting-started">Create a Geometry-Shader Object with Stream Output</a>.
        

The Direct3D 11.1 runtime, which is available starting with Windows 8, provides the following new functionality for <b>CreateGeometryShaderWithStreamOutput</b>.
        

The following shader model 5.0 instructions are available to just pixel shaders and compute shaders in the Direct3D 11.0 runtime. For the Direct3D 11.1 runtime, because unordered access views (UAV) are available at all shader stages, you can use these instructions in all shader stages.

Therefore, if you use the following shader model 5.0 instructions in a geometry shader, you can successfully pass the compiled geometry shader to <i>pShaderBytecode</i>. That is, the call to <b>CreateGeometryShaderWithStreamOutput</b> succeeds.
        

If you pass a compiled shader to <i>pShaderBytecode</i> that uses any of the following instructions on a device that doesn’t support UAVs at every shader stage (including existing drivers that are not implemented to support UAVs at every shader stage), <b>CreateGeometryShaderWithStreamOutput</b> fails.  <b>CreateGeometryShaderWithStreamOutput</b> also fails if the shader tries to use a UAV slot beyond the set of UAV slots that the hardware supports.
        

<ul>
<li>
<a href="/windows/desktop/direct3dhlsl/dcl-uav-typed--sm5---asm-">dcl_uav_typed</a>
</li>
<li>
<a href="/windows/desktop/direct3dhlsl/dcl-uav-raw--sm5---asm-">dcl_uav_raw</a>
</li>
<li>
<a href="/windows/desktop/direct3dhlsl/dcl-uav-structured--sm5---asm-">dcl_uav_structured</a>
</li>
<li>
<a href="/windows/desktop/direct3dhlsl/ld-raw--sm5---asm-">ld_raw</a>
</li>
<li>
<a href="/windows/desktop/direct3dhlsl/ld-structured--sm5---asm-">ld_structured</a>
</li>
<li>
<a href="/windows/desktop/direct3dhlsl/ld-uav-typed--sm5---asm-">ld_uav_typed</a>
</li>
<li>
<a href="/windows/desktop/direct3dhlsl/store-raw--sm5---asm-">store_raw</a>
</li>
<li>
<a href="/windows/desktop/direct3dhlsl/store-structured--sm5---asm-">store_structured</a>
</li>
<li>
<a href="/windows/desktop/direct3dhlsl/store-uav-typed--sm5---asm-">store_uav_typed</a>
</li>
<li>
<a href="/windows/desktop/direct3dhlsl/sync--sm5---asm-">sync_uglobal</a>
</li>
<li>All atomics and immediate atomics (for example, <a href="/windows/desktop/direct3dhlsl/atomic-and--sm5---asm-">atomic_and</a> and <a href="/windows/desktop/direct3dhlsl/imm-atomic-and--sm5---asm-">imm_atomic_and</a>)
          </li>
</ul>
<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>
