---
UID: NF:d3d11.ID3D11Device.CreateComputeShader
title: ID3D11Device::CreateComputeShader (d3d11.h)
description: Create a compute shader.
helpviewer_keywords: ["CreateComputeShader","CreateComputeShader method [Direct3D 11]","CreateComputeShader method [Direct3D 11]","ID3D11Device interface","ID3D11Device interface [Direct3D 11]","CreateComputeShader method","ID3D11Device.CreateComputeShader","ID3D11Device::CreateComputeShader","a7f41890-fbe0-bb14-c192-0d0199550830","d3d11/ID3D11Device::CreateComputeShader","direct3d11.id3d11device_createcomputeshader"]
old-location: direct3d11\id3d11device_createcomputeshader.htm
tech.root: direct3d11
ms.assetid: 4ee0f4f5-48dc-4d5a-b159-c1b7f72e5367
ms.date: 12/05/2018
ms.keywords: CreateComputeShader, CreateComputeShader method [Direct3D 11], CreateComputeShader method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateComputeShader method, ID3D11Device.CreateComputeShader, ID3D11Device::CreateComputeShader, a7f41890-fbe0-bb14-c192-0d0199550830, d3d11/ID3D11Device::CreateComputeShader, direct3d11.id3d11device_createcomputeshader
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
 - ID3D11Device::CreateComputeShader
 - d3d11/ID3D11Device::CreateComputeShader
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
 - ID3D11Device.CreateComputeShader
---

# ID3D11Device::CreateComputeShader


## -description

Create a <a href="/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader">compute shader</a>.

## -parameters

### -param pShaderBytecode [in]

Type: <b>const void*</b>

A pointer to a compiled shader.

### -param BytecodeLength [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

Size of the compiled shader in <i>pShaderBytecode</i>.

### -param pClassLinkage [in, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classlinkage">ID3D11ClassLinkage</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classlinkage">ID3D11ClassLinkage</a>, which represents  class linkage interface; the value can be <b>NULL</b>.

### -param ppComputeShader [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11computeshader">ID3D11ComputeShader</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11computeshader">ID3D11ComputeShader</a> interface. If this is <b>NULL</b>, 
        all other parameters will be validated; if validation passes, CreateComputeShader returns S_FALSE instead of S_OK.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns E_OUTOFMEMORY if there is insufficient memory to create the compute shader.  
        See <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a> for other possible return values.

## -remarks

For an example, see <a href="/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-create">How To: Create a Compute Shader</a> and <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">HDRToneMappingCS11 Sample</a>.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>