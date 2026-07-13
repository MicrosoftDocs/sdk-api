---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.AddStorageFilterEntries
title: ID3D11InfoQueue::AddStorageFilterEntries (d3d11sdklayers.h)
description: Add storage filters to the top of the storage-filter stack. (ID3D11InfoQueue.AddStorageFilterEntries)
helpviewer_keywords: ["931a126d-863e-dd0f-39ba-9205662592db","AddStorageFilterEntries","AddStorageFilterEntries method [Direct3D 11]","AddStorageFilterEntries method [Direct3D 11]","ID3D11InfoQueue interface","ID3D11InfoQueue interface [Direct3D 11]","AddStorageFilterEntries method","ID3D11InfoQueue.AddStorageFilterEntries","ID3D11InfoQueue::AddStorageFilterEntries","d3d11sdklayers/ID3D11InfoQueue::AddStorageFilterEntries","direct3d11.id3d11infoqueue_addstoragefilterentries"]
old-location: direct3d11\id3d11infoqueue_addstoragefilterentries.htm
tech.root: direct3d11
ms.assetid: 18d8a336-44aa-4a21-93c7-e6279bb51853
ms.date: 12/05/2018
ms.keywords: 931a126d-863e-dd0f-39ba-9205662592db, AddStorageFilterEntries, AddStorageFilterEntries method [Direct3D 11], AddStorageFilterEntries method [Direct3D 11],ID3D11InfoQueue interface, ID3D11InfoQueue interface [Direct3D 11],AddStorageFilterEntries method, ID3D11InfoQueue.AddStorageFilterEntries, ID3D11InfoQueue::AddStorageFilterEntries, d3d11sdklayers/ID3D11InfoQueue::AddStorageFilterEntries, direct3d11.id3d11infoqueue_addstoragefilterentries
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
 - ID3D11InfoQueue::AddStorageFilterEntries
 - d3d11sdklayers/ID3D11InfoQueue::AddStorageFilterEntries
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
 - ID3D11InfoQueue.AddStorageFilterEntries
---

# ID3D11InfoQueue::AddStorageFilterEntries


## -description

Add storage filters to the top of the storage-filter stack.

## -parameters

### -param pFilter [in]

Type: <b><a href="/windows/desktop/api/d3d11sdklayers/ns-d3d11sdklayers-d3d11_info_queue_filter">D3D11_INFO_QUEUE_FILTER</a>*</b>

Array of storage filters (see <a href="/windows/desktop/api/d3d11sdklayers/ns-d3d11sdklayers-d3d11_info_queue_filter">D3D11_INFO_QUEUE_FILTER</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11infoqueue">ID3D11InfoQueue Interface</a>
