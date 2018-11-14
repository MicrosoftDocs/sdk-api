---
UID: NF:d3d11.ID3D11Device.CreateGeometryShaderWithStreamOutput
title: ID3D11Device::CreateGeometryShaderWithStreamOutput
author: windows-sdk-content
description: Creates a geometry shader that can write to streaming output buffers.
old-location: direct3d11\id3d11device_creategeometryshaderwithstreamoutput.htm
tech.root: direct3d11
ms.assetid: 69499121-6f35-4cf1-b115-9ffdce26e4b0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 39026c1a-ac13-562f-6f6e-86f1981ebb87, CreateGeometryShaderWithStreamOutput, CreateGeometryShaderWithStreamOutput method [Direct3D 11], CreateGeometryShaderWithStreamOutput method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateGeometryShaderWithStreamOutput method, ID3D11Device.CreateGeometryShaderWithStreamOutput, ID3D11Device::CreateGeometryShaderWithStreamOutput, d3d11/ID3D11Device::CreateGeometryShaderWithStreamOutput, direct3d11.id3d11device_creategeometryshaderwithstreamoutput
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d11.h
: 
- ID3D11Device.CreateGeometryShaderWithStreamOutput
: 
---

# ID3D11Device::CreateGeometryShaderWithStreamOutput


## -description


Creates a geometry shader that can write to streaming output buffers.


## -parameters




### -param pShaderBytecode [in]

Type: <b>const void*</b>

A pointer to the compiled geometry shader for a standard geometry shader plus stream output. For info on how to get this pointer, see <a href="https://msdn.microsoft.com/en-us/library/Bb509703(v=VS.85).aspx">Getting a Pointer to a Compiled Shader</a>.

To create the stream output without using a geometry shader, pass a pointer to the output signature for the prior stage. To obtain this output signature, call the <a href="https://msdn.microsoft.com/en-us/library/Dd607331(v=VS.85).aspx">D3DGetOutputSignatureBlob</a> compiler function. You can also pass a pointer to the compiled shader for the prior stage (for example, the <a href="https://msdn.microsoft.com/library/Bb205146(v=VS.85).aspx">vertex-shader stage</a> or <a href="https://msdn.microsoft.com/en-us/library/Ff476340(v=VS.85).aspx">domain-shader stage</a>). This compiled shader provides the output signature for the data.
            


### -param BytecodeLength [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">SIZE_T</a></b>

Size of the compiled geometry shader.


### -param pSODeclaration [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Ff476216(v=VS.85).aspx">D3D11_SO_DECLARATION_ENTRY</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Ff476216(v=VS.85).aspx">D3D11_SO_DECLARATION_ENTRY</a> array. Cannot be <b>NULL</b> if NumEntries &gt; 0.
          


### -param NumEntries [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The number of entries in the stream output declaration ( ranges from 0 to D3D11_SO_STREAM_COUNT * D3D11_SO_OUTPUT_COMPONENT_COUNT ).


### -param pBufferStrides [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a>*</b>

An array of buffer strides; each stride is the size of an element for that buffer.


### -param NumStrides [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The number of strides (or buffers) in <i>pBufferStrides</i> (ranges from 0 to D3D11_SO_BUFFER_SLOT_COUNT).
          


### -param RasterizedStream [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The index number of the stream to be sent to the rasterizer stage (ranges from 0 to D3D11_SO_STREAM_COUNT - 1).
              Set to D3D11_SO_NO_RASTERIZED_STREAM if no stream is to be rasterized.
            


### -param pClassLinkage [in, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476358(v=VS.85).aspx">ID3D11ClassLinkage</a>*</b>

A pointer to a class linkage interface (see <a href="https://msdn.microsoft.com/en-us/library/Ff476358(v=VS.85).aspx">ID3D11ClassLinkage</a>); the value can be <b>NULL</b>.
          


### -param ppGeometryShader [out, optional]

Type: <b><a href="https://msdn.microsoft.com/c2b5863d-5773-4719-b1d0-2026f55fcef3">ID3D11GeometryShader</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/c2b5863d-5773-4719-b1d0-2026f55fcef3">ID3D11GeometryShader</a> interface, representing the geometry shader that was created.
            Set this to <b>NULL</b> to validate the other parameters; if validation passes, the method will return S_FALSE instead of S_OK.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/en-us/library/Ff476174(v=VS.85).aspx">Direct3D 11 Return Codes</a>.
          




## -remarks



For more info about using <b>CreateGeometryShaderWithStreamOutput</b>, see <a href="https://msdn.microsoft.com/en-us/library/Bb205122(v=VS.85).aspx">Create a Geometry-Shader Object with Stream Output</a>.
        

The Direct3D 11.1 runtime, which is available starting with Windows 8, provides the following new functionality for <b>CreateGeometryShaderWithStreamOutput</b>.
        

The following shader model 5.0 instructions are available to just pixel shaders and compute shaders in the Direct3D 11.0 runtime. For the Direct3D 11.1 runtime, because unordered access views (UAV) are available at all shader stages, you can use these instructions in all shader stages.

Therefore, if you use the following shader model 5.0 instructions in a geometry shader, you can successfully pass the compiled geometry shader to <i>pShaderBytecode</i>. That is, the call to <b>CreateGeometryShaderWithStreamOutput</b> succeeds.
        

If you pass a compiled shader to <i>pShaderBytecode</i> that uses any of the following instructions on a device that doesn’t support UAVs at every shader stage (including existing drivers that are not implemented to support UAVs at every shader stage), <b>CreateGeometryShaderWithStreamOutput</b> fails.  <b>CreateGeometryShaderWithStreamOutput</b> also fails if the shader tries to use a UAV slot beyond the set of UAV slots that the hardware supports.
        

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh446942(v=VS.85).aspx">dcl_uav_typed</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh446938(v=VS.85).aspx">dcl_uav_raw</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh446941(v=VS.85).aspx">dcl_uav_structured</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh447155(v=VS.85).aspx">ld_raw</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh447157(v=VS.85).aspx">ld_structured</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh447160(v=VS.85).aspx">ld_uav_typed</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh447236(v=VS.85).aspx">store_raw</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh447237(v=VS.85).aspx">store_structured</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh447238(v=VS.85).aspx">store_uav_typed</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh447241(v=VS.85).aspx">sync_uglobal</a>
</li>
<li>All atomics and immediate atomics (for example, <a href="https://msdn.microsoft.com/en-us/library/Hh446819(v=VS.85).aspx">atomic_and</a> and <a href="https://msdn.microsoft.com/en-us/library/Hh447118(v=VS.85).aspx">imm_atomic_and</a>)
          </li>
</ul>
<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476379(v=VS.85).aspx">ID3D11Device</a>
 

 

