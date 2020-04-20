---
UID: NF:d3d11.ID3D11Device.CreateVertexShader
title: ID3D11Device::CreateVertexShader (d3d11.h)
description: Create a vertex-shader object from a compiled shader.helpviewer_keywords: ["545fe23c-2bcc-cecf-736c-9a42dd10ee2f","CreateVertexShader","CreateVertexShader method [Direct3D 11]","CreateVertexShader method [Direct3D 11]","ID3D11Device interface","ID3D11Device interface [Direct3D 11]","CreateVertexShader method","ID3D11Device.CreateVertexShader","ID3D11Device::CreateVertexShader","d3d11/ID3D11Device::CreateVertexShader","direct3d11.id3d11device_createvertexshader"]
old-location: direct3d11\id3d11device_createvertexshader.htm
tech.root: direct3d11
ms.assetid: 06e5105a-ff7e-430a-ab9a-2aefb161894c
ms.date: 12/05/2018
ms.keywords: 545fe23c-2bcc-cecf-736c-9a42dd10ee2f, CreateVertexShader, CreateVertexShader method [Direct3D 11], CreateVertexShader method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateVertexShader method, ID3D11Device.CreateVertexShader, ID3D11Device::CreateVertexShader, d3d11/ID3D11Device::CreateVertexShader, direct3d11.id3d11device_createvertexshader
f1_keywords:
- d3d11/ID3D11Device.CreateVertexShader
dev_langs:
- c++
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
- ID3D11Device.CreateVertexShader
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11Device::CreateVertexShader


## -description


Create a vertex-shader object from a compiled shader.


## -parameters




### -param pShaderBytecode [in]

Type: <b>const void*</b>

A pointer to the compiled shader. 


### -param BytecodeLength [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

Size of the compiled vertex shader.


### -param pClassLinkage [in, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11classlinkage">ID3D11ClassLinkage</a>*</b>

A pointer to a class linkage interface (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11classlinkage">ID3D11ClassLinkage</a>); the value can be <b>NULL</b>.


### -param ppVertexShader [out, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader">ID3D11VertexShader</a>**</b>

Address of a pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader">ID3D11VertexShader</a> interface. If this is <b>NULL</b>, all other parameters will be validated, and if all parameters pass validation this API will return <b>S_FALSE</b> instead of <b>S_OK</b>.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.




## -remarks



The Direct3D 11.1 runtime, which is available starting with Windows 8, provides the following new functionality for <b>CreateVertexShader</b>.

The following shader model 5.0 instructions are available to just pixel shaders and compute shaders in the Direct3D 11.0 runtime. For the Direct3D 11.1 runtime, because unordered access views (UAV) are available at all shader stages, you can use these instructions in all shader stages.

Therefore, if you use the following shader model 5.0 instructions in a vertex shader, you can successfully pass the compiled vertex shader to <i>pShaderBytecode</i>. That is, the call to <b>CreateVertexShader</b> succeeds.

If you pass a compiled shader to <i>pShaderBytecode</i> that uses any of the following instructions on a device that doesn’t support UAVs at every shader stage (including existing drivers that are not implemented to support UAVs at every shader stage), <b>CreateVertexShader</b> fails.  <b>CreateVertexShader</b> also fails if the shader tries to use a UAV slot beyond the set of UAV slots that the hardware supports.

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/dcl-uav-typed--sm5---asm-">dcl_uav_typed</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/dcl-uav-raw--sm5---asm-">dcl_uav_raw</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/dcl-uav-structured--sm5---asm-">dcl_uav_structured</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/ld-raw--sm5---asm-">ld_raw</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/ld-structured--sm5---asm-">ld_structured</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/ld-uav-typed--sm5---asm-">ld_uav_typed</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/store-raw--sm5---asm-">store_raw</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/store-structured--sm5---asm-">store_structured</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/store-uav-typed--sm5---asm-">store_uav_typed</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/sync--sm5---asm-">sync_uglobal</a>
</li>
<li>All atomics and immediate atomics (for example, <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/atomic-and--sm5---asm-">atomic_and</a> and <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/imm-atomic-and--sm5---asm-">imm_atomic_and</a>)</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>
 

 

