---
UID: NF:d3dcompiler.D3DGetBlobPart
title: D3DGetBlobPart function (d3dcompiler.h)
author: windows-sdk-content
description: Retrieves a specific part from a compilation result.
old-location: direct3dhlsl\d3dgetblobpart.htm
tech.root: direct3dhlsl
ms.assetid: cf9cea53-e7a3-4473-bfdf-0cdeb8370974
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3DGetBlobPart, D3DGetBlobPart function [HLSL], d3dcompiler/D3DGetBlobPart, direct3dhlsl.d3dgetblobpart
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
 - D3DGetBlobPart
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# D3DGetBlobPart function


## -description


Retrieves a specific part from a compilation result.


## -parameters




### -param pSrcData [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCVOID</a></b>

A pointer to uncompiled shader data; either ASCII HLSL code or a compiled effect.


### -param SrcDataSize [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Length of uncompiled shader data that <i>pSrcData</i> points to.


### -param Part [in]

Type: <b><a href="https://msdn.microsoft.com/333bc68a-0412-48e7-ac28-69ec5eea9ce8">D3D_BLOB_PART</a></b>

A <a href="https://msdn.microsoft.com/333bc68a-0412-48e7-ac28-69ec5eea9ce8">D3D_BLOB_PART</a>-typed value that specifies the part of the buffer to retrieve.


### -param Flags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Flags that indicate how to retrieve the blob part. Currently, no flags are defined.


### -param ppPart [out]

Type: <b><a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a>**</b>

The address of a pointer to the <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> interface that is used to retrieve the specified part of the buffer.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 return codes</a>.




## -remarks



<b>D3DGetBlobPart</b> retrieves the part of a blob (arbitrary length data buffer) that contains the type of data that the  <i>Part</i> parameter specifies.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd607342(v=VS.85).aspx">Functions</a>
 

 

