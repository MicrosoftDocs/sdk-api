---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.PushRetrievalFilter
title: ID3D11InfoQueue::PushRetrievalFilter (d3d11sdklayers.h)
description: Push a retrieval filter onto the retrieval-filter stack. (ID3D11InfoQueue.PushRetrievalFilter)
helpviewer_keywords: ["227e4e96-44d1-fd15-2776-9f57074da42a","ID3D11InfoQueue interface [Direct3D 11]","PushRetrievalFilter method","ID3D11InfoQueue.PushRetrievalFilter","ID3D11InfoQueue::PushRetrievalFilter","PushRetrievalFilter","PushRetrievalFilter method [Direct3D 11]","PushRetrievalFilter method [Direct3D 11]","ID3D11InfoQueue interface","d3d11sdklayers/ID3D11InfoQueue::PushRetrievalFilter","direct3d11.id3d11infoqueue_pushretrievalfilter"]
old-location: direct3d11\id3d11infoqueue_pushretrievalfilter.htm
tech.root: direct3d11
ms.assetid: ba0ff492-bd35-499a-972c-135593e84fea
ms.date: 12/05/2018
ms.keywords: 227e4e96-44d1-fd15-2776-9f57074da42a, ID3D11InfoQueue interface [Direct3D 11],PushRetrievalFilter method, ID3D11InfoQueue.PushRetrievalFilter, ID3D11InfoQueue::PushRetrievalFilter, PushRetrievalFilter, PushRetrievalFilter method [Direct3D 11], PushRetrievalFilter method [Direct3D 11],ID3D11InfoQueue interface, d3d11sdklayers/ID3D11InfoQueue::PushRetrievalFilter, direct3d11.id3d11infoqueue_pushretrievalfilter
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
 - ID3D11InfoQueue::PushRetrievalFilter
 - d3d11sdklayers/ID3D11InfoQueue::PushRetrievalFilter
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
 - ID3D11InfoQueue.PushRetrievalFilter
---

# ID3D11InfoQueue::PushRetrievalFilter


## -description

Push a retrieval filter onto the retrieval-filter stack.

## -parameters

### -param pFilter [in]

Type: <b><a href="/windows/desktop/api/d3d11sdklayers/ns-d3d11sdklayers-d3d11_info_queue_filter">D3D11_INFO_QUEUE_FILTER</a>*</b>

Pointer to a retrieval filter (see <a href="/windows/desktop/api/d3d11sdklayers/ns-d3d11sdklayers-d3d11_info_queue_filter">D3D11_INFO_QUEUE_FILTER</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11infoqueue">ID3D11InfoQueue Interface</a>
