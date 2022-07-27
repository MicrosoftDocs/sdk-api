---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.PushStorageFilter
title: ID3D11InfoQueue::PushStorageFilter (d3d11sdklayers.h)
description: Push a storage filter onto the storage-filter stack. (ID3D11InfoQueue.PushStorageFilter)
helpviewer_keywords: ["8aa4344e-4688-6e7c-8033-8b589f37ce3d","ID3D11InfoQueue interface [Direct3D 11]","PushStorageFilter method","ID3D11InfoQueue.PushStorageFilter","ID3D11InfoQueue::PushStorageFilter","PushStorageFilter","PushStorageFilter method [Direct3D 11]","PushStorageFilter method [Direct3D 11]","ID3D11InfoQueue interface","d3d11sdklayers/ID3D11InfoQueue::PushStorageFilter","direct3d11.id3d11infoqueue_pushstoragefilter"]
old-location: direct3d11\id3d11infoqueue_pushstoragefilter.htm
tech.root: direct3d11
ms.assetid: de3f22b0-0642-4aa8-8bb0-008c1e44d3cb
ms.date: 12/05/2018
ms.keywords: 8aa4344e-4688-6e7c-8033-8b589f37ce3d, ID3D11InfoQueue interface [Direct3D 11],PushStorageFilter method, ID3D11InfoQueue.PushStorageFilter, ID3D11InfoQueue::PushStorageFilter, PushStorageFilter, PushStorageFilter method [Direct3D 11], PushStorageFilter method [Direct3D 11],ID3D11InfoQueue interface, d3d11sdklayers/ID3D11InfoQueue::PushStorageFilter, direct3d11.id3d11infoqueue_pushstoragefilter
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
 - ID3D11InfoQueue::PushStorageFilter
 - d3d11sdklayers/ID3D11InfoQueue::PushStorageFilter
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
 - ID3D11InfoQueue.PushStorageFilter
---

# ID3D11InfoQueue::PushStorageFilter


## -description

Push a storage filter onto the storage-filter stack.

## -parameters

### -param pFilter [in]

Type: <b><a href="/windows/desktop/api/d3d11sdklayers/ns-d3d11sdklayers-d3d11_info_queue_filter">D3D11_INFO_QUEUE_FILTER</a>*</b>

Pointer to a storage filter (see <a href="/windows/desktop/api/d3d11sdklayers/ns-d3d11sdklayers-d3d11_info_queue_filter">D3D11_INFO_QUEUE_FILTER</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11infoqueue">ID3D11InfoQueue Interface</a>
