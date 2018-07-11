---
UID: NF:d3d10misc.D3D10CreateBlob
title: D3D10CreateBlob function
author: windows-sdk-content
description: Create a buffer.Note  Instead of using this function, we recommend that you use the D3DCreateBlob API.
old-location: direct3d10\d3d10createblob.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10createblob.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: 5f032879-d10b-8a54-5b40-9fa1e178b0d5, D3D10CreateBlob, D3D10CreateBlob function [Direct3D 10], d3d10misc/D3D10CreateBlob, direct3d10.d3d10createblob
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: d3d10misc.h
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
req.typenames: D3D10_DRIVER_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D10.dll
api_name:
 - D3D10CreateBlob
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
---

# D3D10CreateBlob function


## -description


Create a buffer.
<div class="alert"><b>Note</b>  Instead of using this function, we recommend that you use the <a href="https://msdn.microsoft.com/9cad9bff-1641-4fb1-a7c9-c3e31089d7f7">D3DCreateBlob</a> API.</div><div> </div>

## -parameters




### -param NumBytes [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Number of bytes in the blob.


### -param ppBuffer [out]

Type: <b><a href="https://msdn.microsoft.com/d180fee0-1a69-4250-a0c4-d6e3754f063a">LPD3D10BLOB</a>*</b>

The address of a pointer to the buffer (see <a href="https://msdn.microsoft.com/d180fee0-1a69-4250-a0c4-d6e3754f063a">ID3D10Blob Interface</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/012577cd-970e-43bc-996e-3be7c2283b60">Core Functions</a>
 

 

