---
UID: NF:d3dcompiler.D3DCompressShaders
title: D3DCompressShaders function
author: windows-sdk-content
description: Compresses a set of shaders into a more compact form.
old-location: direct3dhlsl\d3dcompressshaders.htm
tech.root: direct3dhlsl
ms.assetid: e53a0d36-3cd4-4327-8969-6a864b38a15b
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: D3DCompressShaders, D3DCompressShaders function [HLSL], d3dcompiler/D3DCompressShaders, direct3dhlsl.d3dcompressshaders
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d3dcompiler.h
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
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3DCompiler_47.dll
api_name:
 - D3DCompressShaders
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- D3DCompressShaders
: 
---

# D3DCompressShaders function


## -description


<div class="alert"><b>Note</b>  You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</div><div> </div>Compresses a set of shaders into a more compact form. 


## -parameters




### -param uNumShaders [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of shaders to compress.


### -param pShaderData [in]

Type: <b><a href="https://msdn.microsoft.com/34cde0c9-e8ee-428d-86f5-87c91b95f5d8">D3D_SHADER_DATA</a>*</b>

An array of <a href="https://msdn.microsoft.com/34cde0c9-e8ee-428d-86f5-87c91b95f5d8">D3D_SHADER_DATA</a> structures that describe the set of shaders to compress.


### -param uFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Flags that indicate how to compress the shaders. Currently, only the  D3D_COMPRESS_SHADER_KEEP_ALL_PARTS (0x00000001) flag is defined.


### -param ppCompressedData [out]

Type: <b><a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a>**</b>

The address of a pointer to the <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> interface that is used to retrieve the compressed shader data.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 return codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/aacc5207-3ec8-4031-b5c9-f7c0fb7b7095">Functions</a>
 

 

