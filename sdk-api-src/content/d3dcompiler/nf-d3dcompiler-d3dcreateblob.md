---
UID: NF:d3dcompiler.D3DCreateBlob
title: D3DCreateBlob function
author: windows-sdk-content
description: Creates a buffer.
old-location: direct3dhlsl\d3dcreateblob.htm
old-project: direct3dhlsl
ms.assetid: 9cad9bff-1641-4fb1-a7c9-c3e31089d7f7
ms.author: windowssdkdev
ms.date: 04/12/2018
ms.keywords: D3DCreateBlob, D3DCreateBlob function [HLSL], d3dcompiler/D3DCreateBlob, direct3dhlsl.d3dcreateblob
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: D3D_BLOB_PART
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	D3DCompiler_47.dll
api_name:
-	D3DCreateBlob
product: Windows
targetos: Windows
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
---

# D3DCreateBlob function


## -description


Creates a buffer.


## -parameters




### -param Size [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Number of bytes in the blob.


### -param ppBlob [out]

Type: <b><a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a>**</b>

The address of a pointer to the <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> interface that is used to retrieve the buffer.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 return codes</a>.




## -remarks



The latest D3dcompiler_nn.dll contains the <b>D3DCreateBlob</b> compiler function. Therefore, you are no longer required to create and use an arbitrary length data buffer by using the  <a href="https://msdn.microsoft.com/bacc1d17-13e2-428c-9fd5-01c02406aa14">D3D10CreateBlob</a> function that is contained in D3d10.dll.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

