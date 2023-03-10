---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.AddStorageFilterEntries
title: ID3D12InfoQueue::AddStorageFilterEntries (d3d12sdklayers.h)
description: Add storage filters to the top of the storage-filter stack. (ID3D12InfoQueue.AddStorageFilterEntries)
helpviewer_keywords: ["AddStorageFilterEntries","AddStorageFilterEntries method","AddStorageFilterEntries method","ID3D12InfoQueue interface","ID3D12InfoQueue interface","AddStorageFilterEntries method","ID3D12InfoQueue.AddStorageFilterEntries","ID3D12InfoQueue::AddStorageFilterEntries","d3d12sdklayers/ID3D12InfoQueue::AddStorageFilterEntries","direct3d12.id3d12infoqueue_addstoragefilterentries"]
old-location: direct3d12\id3d12infoqueue_addstoragefilterentries.htm
tech.root: direct3d12
ms.assetid: 24AEAE62-D2D8-4A0C-9EB3-6D3942BC86D9
ms.date: 12/05/2018
ms.keywords: AddStorageFilterEntries, AddStorageFilterEntries method, AddStorageFilterEntries method,ID3D12InfoQueue interface, ID3D12InfoQueue interface,AddStorageFilterEntries method, ID3D12InfoQueue.AddStorageFilterEntries, ID3D12InfoQueue::AddStorageFilterEntries, d3d12sdklayers/ID3D12InfoQueue::AddStorageFilterEntries, direct3d12.id3d12infoqueue_addstoragefilterentries
req.header: d3d12sdklayers.h
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
 - ID3D12InfoQueue::AddStorageFilterEntries
 - d3d12sdklayers/ID3D12InfoQueue::AddStorageFilterEntries
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12InfoQueue.AddStorageFilterEntries
---

# ID3D12InfoQueue::AddStorageFilterEntries


## -description

Add storage filters to the top of the storage-filter stack.

## -parameters

### -param pFilter [in]

Type: <b><a href="/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter">D3D12_INFO_QUEUE_FILTER</a>*</b>

Array of storage filters.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue">ID3D12InfoQueue</a>
