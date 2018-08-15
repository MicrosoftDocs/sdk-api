---
UID: NF:d3dcompiler.D3DDecompressShaders
title: D3DDecompressShaders function
author: windows-sdk-content
description: Decompresses one or more shaders from a compressed set.
old-location: direct3dhlsl\d3ddecompressshaders.htm
old-project: direct3dhlsl
ms.assetid: 9b62026f-0658-405c-8f45-ee921213148a
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: D3DDecompressShaders, D3DDecompressShaders function [HLSL], d3dcompiler/D3DDecompressShaders, direct3dhlsl.d3ddecompressshaders
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: d3dcompiler.h
req.include-header: 
req.redist: 
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
req.typenames: D3D_BLOB_PART
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3DCompiler_47.dll
api_name:
 - D3DDecompressShaders
product: Windows
targetos: Windows
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
---

# D3DDecompressShaders function


## -description


<div class="alert"><b>Note</b>  You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</div><div> </div>Decompresses one or more shaders from a compressed set. 


## -parameters




### -param pSrcData [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCVOID</a></b>

A pointer to uncompiled shader data; either ASCII HLSL code or a compiled effect.


### -param SrcDataSize [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Length of uncompiled shader data that <i>pSrcData</i> points to.


### -param uNumShaders [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of shaders to decompress.


### -param uStartIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the first shader to decompress.


### -param pIndices [in, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

An array of indexes that represent the shaders to decompress.


### -param uFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Flags that indicate how to decompress. Currently, no flags are defined.


### -param ppShaders [out]

Type: <b><a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a>**</b>

The address of a pointer to the <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> interface that is used to retrieve the decompressed shader data.


### -param pTotalShaders [out, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

A pointer to a variable that receives the total number of shaders that  <b>D3DDecompressShaders</b> decompressed.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 return codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/aacc5207-3ec8-4031-b5c9-f7c0fb7b7095">Functions</a>
 

 

