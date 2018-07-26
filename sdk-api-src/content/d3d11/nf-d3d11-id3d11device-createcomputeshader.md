---
UID: NF:d3d11.ID3D11Device.CreateComputeShader
title: ID3D11Device::CreateComputeShader
author: windows-sdk-content
description: Create a compute shader.
old-location: direct3d11\id3d11device_createcomputeshader.htm
old-project: direct3d11
ms.assetid: 4ee0f4f5-48dc-4d5a-b159-c1b7f72e5367
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: CreateComputeShader, CreateComputeShader method [Direct3D 11], CreateComputeShader method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateComputeShader method, ID3D11Device.CreateComputeShader, ID3D11Device::CreateComputeShader, a7f41890-fbe0-bb14-c192-0d0199550830, d3d11/ID3D11Device::CreateComputeShader, direct3d11.id3d11device_createcomputeshader
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D11_VPOV_DIMENSION
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
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Device::CreateComputeShader


## -description


Create a <a href="https://msdn.microsoft.com/02c1f98e-fdd6-49b0-b8b2-efbd472ab599">compute shader</a>.


## -parameters




### -param pShaderBytecode [in]

Type: <b>const void*</b>

A pointer to a compiled shader.


### -param BytecodeLength [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Size of the compiled shader in <i>pShaderBytecode</i>.


### -param pClassLinkage [in, optional]

Type: <b><a href="https://msdn.microsoft.com/eac03911-d881-4304-9598-912321ac0b0c">ID3D11ClassLinkage</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/eac03911-d881-4304-9598-912321ac0b0c">ID3D11ClassLinkage</a>, which represents  class linkage interface; the value can be <b>NULL</b>.


### -param ppComputeShader [out, optional]

Type: <b><a href="https://msdn.microsoft.com/33a43253-ada2-4085-9401-e84562b37d59">ID3D11ComputeShader</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/33a43253-ada2-4085-9401-e84562b37d59">ID3D11ComputeShader</a> interface. If this is <b>NULL</b>, 
        all other parameters will be validated; if validation passes, CreateComputeShader returns S_FALSE instead of S_OK.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns E_OUTOFMEMORY if there is insufficient memory to create the compute shader.  
        See <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a> for other possible return values.




## -remarks



For an example, see <a href="https://msdn.microsoft.com/6114dd90-626b-4c9e-9da5-7d2d33153e79">How To: Create a Compute Shader</a> and <a href="d325cd30-56e1-d608-6ab6-2755caf2b1b1">HDRToneMappingCS11 Sample</a>.




## -see-also




<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
 

 

