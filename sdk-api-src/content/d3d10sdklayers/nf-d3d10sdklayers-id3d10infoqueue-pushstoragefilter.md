---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.PushStorageFilter
title: ID3D10InfoQueue::PushStorageFilter (d3d10sdklayers.h)
description: Push a storage filter onto the storage-filter stack. (ID3D10InfoQueue.PushStorageFilter)
helpviewer_keywords: ["ID3D10InfoQueue interface [Direct3D 10]","PushStorageFilter method","ID3D10InfoQueue.PushStorageFilter","ID3D10InfoQueue::PushStorageFilter","PushStorageFilter","PushStorageFilter method [Direct3D 10]","PushStorageFilter method [Direct3D 10]","ID3D10InfoQueue interface","d3d10sdklayers/ID3D10InfoQueue::PushStorageFilter","direct3d10.id3d10infoqueue_pushstoragefilter","f8b3ecae-90a5-7c55-1e43-1a305aafd928"]
old-location: direct3d10\id3d10infoqueue_pushstoragefilter.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_pushstoragefilter.htm
ms.date: 12/05/2018
ms.keywords: ID3D10InfoQueue interface [Direct3D 10],PushStorageFilter method, ID3D10InfoQueue.PushStorageFilter, ID3D10InfoQueue::PushStorageFilter, PushStorageFilter, PushStorageFilter method [Direct3D 10], PushStorageFilter method [Direct3D 10],ID3D10InfoQueue interface, d3d10sdklayers/ID3D10InfoQueue::PushStorageFilter, direct3d10.id3d10infoqueue_pushstoragefilter, f8b3ecae-90a5-7c55-1e43-1a305aafd928
req.header: d3d10sdklayers.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10InfoQueue::PushStorageFilter
 - d3d10sdklayers/ID3D10InfoQueue::PushStorageFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10SDKLayers.h
api_name:
 - ID3D10InfoQueue.PushStorageFilter
---

# ID3D10InfoQueue::PushStorageFilter


## -description

Push a storage filter onto the storage-filter stack.

## -parameters

### -param pFilter [in]

Type: <b><a href="/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter">D3D10_INFO_QUEUE_FILTER</a>*</b>

Pointer to a storage filter (see <a href="/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter">D3D10_INFO_QUEUE_FILTER</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d10sdklayers/nn-d3d10sdklayers-id3d10infoqueue">ID3D10InfoQueue Interface</a>
