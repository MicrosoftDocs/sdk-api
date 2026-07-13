---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.GetRetrievalFilter
title: ID3D11InfoQueue::GetRetrievalFilter (d3d11sdklayers.h)
description: Get the retrieval filter at the top of the retrieval-filter stack. (ID3D11InfoQueue.GetRetrievalFilter)
helpviewer_keywords: ["5e162a9f-4e8f-4852-65fb-df19d695af47","GetRetrievalFilter","GetRetrievalFilter method [Direct3D 11]","GetRetrievalFilter method [Direct3D 11]","ID3D11InfoQueue interface","ID3D11InfoQueue interface [Direct3D 11]","GetRetrievalFilter method","ID3D11InfoQueue.GetRetrievalFilter","ID3D11InfoQueue::GetRetrievalFilter","d3d11sdklayers/ID3D11InfoQueue::GetRetrievalFilter","direct3d11.id3d11infoqueue_getretrievalfilter"]
old-location: direct3d11\id3d11infoqueue_getretrievalfilter.htm
tech.root: direct3d11
ms.assetid: bbf05fe7-91b7-40ce-895c-82e60fa456e9
ms.date: 12/05/2018
ms.keywords: 5e162a9f-4e8f-4852-65fb-df19d695af47, GetRetrievalFilter, GetRetrievalFilter method [Direct3D 11], GetRetrievalFilter method [Direct3D 11],ID3D11InfoQueue interface, ID3D11InfoQueue interface [Direct3D 11],GetRetrievalFilter method, ID3D11InfoQueue.GetRetrievalFilter, ID3D11InfoQueue::GetRetrievalFilter, d3d11sdklayers/ID3D11InfoQueue::GetRetrievalFilter, direct3d11.id3d11infoqueue_getretrievalfilter
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11InfoQueue::GetRetrievalFilter
 - d3d11sdklayers/ID3D11InfoQueue::GetRetrievalFilter
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
 - ID3D11InfoQueue.GetRetrievalFilter
---

# ID3D11InfoQueue::GetRetrievalFilter


## -description

Get the retrieval filter at the top of the retrieval-filter stack.

## -parameters

### -param pFilter [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11sdklayers/ns-d3d11sdklayers-d3d11_info_queue_filter">D3D11_INFO_QUEUE_FILTER</a>*</b>

Retrieval filter at the top of the retrieval-filter stack.

### -param pFilterByteLength [in, out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a>*</b>

Size of the retrieval filter in bytes. If pFilter is <b>NULL</b>, the size of the retrieval filter will be output to this parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11infoqueue">ID3D11InfoQueue Interface</a>
