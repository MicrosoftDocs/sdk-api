---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.GetRetrievalFilter
title: ID3D11InfoQueue::GetRetrievalFilter
author: windows-sdk-content
description: Get the retrieval filter at the top of the retrieval-filter stack.
old-location: direct3d11\id3d11infoqueue_getretrievalfilter.htm
tech.root: direct3d11
ms.assetid: bbf05fe7-91b7-40ce-895c-82e60fa456e9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 5e162a9f-4e8f-4852-65fb-df19d695af47, GetRetrievalFilter, GetRetrievalFilter method [Direct3D 11], GetRetrievalFilter method [Direct3D 11],ID3D11InfoQueue interface, ID3D11InfoQueue interface [Direct3D 11],GetRetrievalFilter method, ID3D11InfoQueue.GetRetrievalFilter, ID3D11InfoQueue::GetRetrievalFilter, d3d11sdklayers/ID3D11InfoQueue::GetRetrievalFilter, direct3d11.id3d11infoqueue_getretrievalfilter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11sdklayers.h
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
 - ID3D11InfoQueue.GetRetrievalFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11InfoQueue::GetRetrievalFilter


## -description


Get the retrieval filter at the top of the retrieval-filter stack.


## -parameters




### -param pFilter [out, optional]

Type: <b><a href="https://msdn.microsoft.com/6ff12751-86dd-4ae0-b532-661a70dad21f">D3D11_INFO_QUEUE_FILTER</a>*</b>

Retrieval filter at the top of the retrieval-filter stack.


### -param pFilterByteLength [in, out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a>*</b>

Size of the retrieval filter in bytes. If pFilter is <b>NULL</b>, the size of the retrieval filter will be output to this parameter.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/240820c7-1c1f-4e2d-8b3e-497fd931d7d2">ID3D11InfoQueue Interface</a>
 

 

