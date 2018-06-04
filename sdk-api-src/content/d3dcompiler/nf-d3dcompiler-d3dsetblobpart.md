---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# D3DSetBlobPart function


## -description


Sets information in a compilation result.


## -parameters




### -param pSrcData [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCVOID</a></b>

A pointer to compiled shader data.


### -param SrcDataSize [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

The length of the compiled shader data that <i>pSrcData</i> points to.


### -param Part [in]

Type: <b><a href="https://msdn.microsoft.com/333bc68a-0412-48e7-ac28-69ec5eea9ce8">D3D_BLOB_PART</a></b>

A <a href="https://msdn.microsoft.com/333bc68a-0412-48e7-ac28-69ec5eea9ce8">D3D_BLOB_PART</a>-typed value that specifies the part to set. Currently, you can update only private data; that is, <b>D3DSetBlobPart</b> currently only supports the <a href="d3d_blob_part.htm">D3D_BLOB_PRIVATE_DATA</a> value.


### -param Flags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Flags that indicate how to set the blob part. Currently, no flags are defined; therefore, set to zero.


### -param pPart [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCVOID</a></b>

A pointer to data to set in the compilation result.


### -param PartSize [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

The length of the data that <i>pPart</i> points to.


### -param ppNewShader [out]

Type: <b><a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a>**</b>

A pointer to a buffer that receives the <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> interface for the new shader in which the new part data is set.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 return codes</a>.




## -remarks



<b>D3DSetBlobPart</b> modifies data in a compiled shader.  Currently, <b>D3DSetBlobPart</b> can update only the private data in a compiled shader. You can use  <b>D3DSetBlobPart</b> to attach arbitrary uninterpreted data to a compiled shader.

<div class="alert"><b>Note</b>  The D3dcompiler_44.dll or later version of the file contains the <b>D3DSetBlobPart</b> compiler function.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

