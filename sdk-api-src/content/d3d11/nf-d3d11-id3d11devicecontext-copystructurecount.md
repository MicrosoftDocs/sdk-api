---
UID: NF:d3d11.ID3D11DeviceContext.CopyStructureCount
title: ID3D11DeviceContext::CopyStructureCount
author: windows-sdk-content
description: Copies data from a buffer holding variable length data.
old-location: direct3d11\id3d11devicecontext_copystructurecount.htm
tech.root: direct3d11
ms.assetid: d4f8576f-8d23-4b45-a5ea-099c71e8567e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CopyStructureCount, CopyStructureCount method [Direct3D 11], CopyStructureCount method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],CopyStructureCount method, ID3D11DeviceContext.CopyStructureCount, ID3D11DeviceContext::CopyStructureCount, d3d11/ID3D11DeviceContext::CopyStructureCount, d927d44d-491d-b350-cc6e-49cfd29f1793, direct3d11.id3d11devicecontext_copystructurecount
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID3D11DeviceContext.CopyStructureCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext::CopyStructureCount


## -description


Copies data from a buffer holding variable length data.


## -parameters




### -param pDstBuffer [in]

Type: <b><a href="https://msdn.microsoft.com/7224de57-75cb-4d68-9d70-f5dd2f92b1fd">ID3D11Buffer</a>*</b>

Pointer to <a href="https://msdn.microsoft.com/7224de57-75cb-4d68-9d70-f5dd2f92b1fd">ID3D11Buffer</a>.  This can be any buffer resource that other copy commands, 
        such as <a href="https://msdn.microsoft.com/54c1c08a-792c-463d-8237-9f7947d15396">ID3D11DeviceContext::CopyResource</a> or <a href="https://msdn.microsoft.com/aed89483-9870-445d-96e3-a9cee764f0ad">ID3D11DeviceContext::CopySubresourceRegion</a>, are able to write to.


### -param DstAlignedByteOffset [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset from the start of <i>pDstBuffer</i> to write 32-bit UINT structure (vertex) count from <i>pSrcView</i>.


### -param pSrcView [in]

Type: <b><a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a> of a Structured Buffer resource created with either 
        <a href="https://msdn.microsoft.com/13cf0083-c61a-478d-94bd-00dec4cf27b7">D3D11_BUFFER_UAV_FLAG_APPEND</a> or <b>D3D11_BUFFER_UAV_FLAG_COUNTER</b> specified 
        when the UAV was created.   These types of resources have hidden counters tracking "how many" records have 
        been written.


## -returns



Returns nothing.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

