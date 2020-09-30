---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.GetStorageFilter
title: ID3D10InfoQueue::GetStorageFilter (d3d10sdklayers.h)
description: Get the storage filter at the top of the storage-filter stack.
helpviewer_keywords: ["2a5b558d-3526-acaa-1d02-32a867241cae","GetStorageFilter","GetStorageFilter method [Direct3D 10]","GetStorageFilter method [Direct3D 10]","ID3D10InfoQueue interface","ID3D10InfoQueue interface [Direct3D 10]","GetStorageFilter method","ID3D10InfoQueue.GetStorageFilter","ID3D10InfoQueue::GetStorageFilter","d3d10sdklayers/ID3D10InfoQueue::GetStorageFilter","direct3d10.id3d10infoqueue_getstoragefilter"]
old-location: direct3d10\id3d10infoqueue_getstoragefilter.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_getstoragefilter.htm
ms.date: 12/05/2018
ms.keywords: 2a5b558d-3526-acaa-1d02-32a867241cae, GetStorageFilter, GetStorageFilter method [Direct3D 10], GetStorageFilter method [Direct3D 10],ID3D10InfoQueue interface, ID3D10InfoQueue interface [Direct3D 10],GetStorageFilter method, ID3D10InfoQueue.GetStorageFilter, ID3D10InfoQueue::GetStorageFilter, d3d10sdklayers/ID3D10InfoQueue::GetStorageFilter, direct3d10.id3d10infoqueue_getstoragefilter
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
 - ID3D10InfoQueue::GetStorageFilter
 - d3d10sdklayers/ID3D10InfoQueue::GetStorageFilter
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
 - ID3D10InfoQueue.GetStorageFilter
---

# ID3D10InfoQueue::GetStorageFilter


## -description

Get the storage filter at the top of the storage-filter stack.

## -parameters

### -param pFilter [out]

Type: <b><a href="/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter">D3D10_INFO_QUEUE_FILTER</a>*</b>

Storage filter at the top of the storage-filter stack.

### -param pFilterByteLength [in, out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a>*</b>

Size of the storage filter in bytes. If pFilter is <b>NULL</b>, the size of the storage filter will be output to this parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d10sdklayers/nn-d3d10sdklayers-id3d10infoqueue">ID3D10InfoQueue Interface</a>