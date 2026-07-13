---
UID: NF:d3d11.ID3D11Device.CreateGeometryShader
title: ID3D11Device::CreateGeometryShader (d3d11.h)
description: Create a geometry shader. (ID3D11Device.CreateGeometryShader)
helpviewer_keywords: ["CreateGeometryShader","CreateGeometryShader method [Direct3D 11]","CreateGeometryShader method [Direct3D 11]","ID3D11Device interface","ID3D11Device interface [Direct3D 11]","CreateGeometryShader method","ID3D11Device.CreateGeometryShader","ID3D11Device::CreateGeometryShader","c0fe27f5-e83c-fa7e-faca-a34ea90a0c53","d3d11/ID3D11Device::CreateGeometryShader","direct3d11.id3d11device_creategeometryshader"]
old-location: direct3d11\id3d11device_creategeometryshader.htm
tech.root: direct3d11
ms.assetid: fb9357d7-ac63-4515-9118-24a2d775e697
ms.date: 12/05/2018
ms.keywords: CreateGeometryShader, CreateGeometryShader method [Direct3D 11], CreateGeometryShader method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateGeometryShader method, ID3D11Device.CreateGeometryShader, ID3D11Device::CreateGeometryShader, c0fe27f5-e83c-fa7e-faca-a34ea90a0c53, d3d11/ID3D11Device::CreateGeometryShader, direct3d11.id3d11device_creategeometryshader
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
 - ID3D11Device::CreateGeometryShader
 - d3d11/ID3D11Device::CreateGeometryShader
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
 - ID3D11Device.CreateGeometryShader
---

# ID3D11Device::CreateGeometryShader


## -description

Create a geometry shader.

## -parameters

### -param pShaderBytecode [in]

Type: <b>const void*</b>

A pointer to the compiled shader.

### -param BytecodeLength [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

Size of the compiled geometry shader.

### -param pClassLinkage [in, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classlinkage">ID3D11ClassLinkage</a>*</b>

A pointer to a class linkage interface (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classlinkage">ID3D11ClassLinkage</a>); the value can be <b>NULL</b>.

### -param ppGeometryShader [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader">ID3D11GeometryShader</a>**</b>

Address of a pointer to a <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader">ID3D11GeometryShader</a> interface. If this is <b>NULL</b>, all other parameters will be validated, and if all
        parameters pass validation this API will return S_FALSE instead of S_OK.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

After it is created, the shader can be set to the device by calling <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-gssetshader">ID3D11DeviceContext::GSSetShader</a>.

The Direct3D 11.1 runtime, which is available starting with Windows 8, provides the following new functionality for <b>CreateGeometryShader</b>.

The following shader model 5.0 instructions are available to just pixel shaders and compute shaders in the Direct3D 11.0 runtime. For the Direct3D 11.1 runtime, because unordered access views (UAV) are available at all shader stages, you can use these instructions in all shader stages.

Therefore, if you use the following shader model 5.0 instructions in a geometry shader, you can successfully pass the compiled geometry shader to <i>pShaderBytecode</i>. That is, the call to <b>CreateGeometryShader</b> succeeds.

If you pass a compiled shader to <i>pShaderBytecode</i> that uses any of the following instructions on a device that doesn’t support UAVs at every shader stage (including existing drivers that are not implemented to support UAVs at every shader stage), <b>CreateGeometryShader</b> fails.  <b>CreateGeometryShader</b> also fails if the shader tries to use a UAV slot beyond the set of UAV slots that the hardware supports.

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
<li>All atomics and immediate atomics (for example, <a href="/windows/desktop/direct3dhlsl/atomic-and--sm5---asm-">atomic_and</a> and <a href="/windows/desktop/direct3dhlsl/imm-atomic-and--sm5---asm-">imm_atomic_and</a>)</li>
</ul>

#### Examples

Usage Example


```

ID3D11GeometryShader*       g_pGeometryShader11 = NULL;
ID3DBlob* pGeometryShaderBuffer = NULL;
ID3DBlob * errorbuffer = NULL;

D3DX11CompileFromFile( str, NULL, NULL, "GS", "gs_4_0", dwShaderFlags, 0, NULL,
                                         &pGeometryShaderBuffer, &errorbuffer, NULL );

pd3dDevice->CreateGeometryShader( pGeometryShaderBuffer->GetBufferPointer(),
               pGeometryShaderBuffer->GetBufferSize(), NULL, &g_pGeometryShader11 );
     
          
```

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>
