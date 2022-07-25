---
UID: NF:d3d12.ID3D12Resource.Unmap
title: ID3D12Resource::Unmap (d3d12.h)
description: Invalidates the CPU pointer to the specified subresource in the resource.
helpviewer_keywords: ["ID3D12Resource interface","Unmap method","ID3D12Resource.Unmap","ID3D12Resource::Unmap","Unmap","Unmap method","Unmap method","ID3D12Resource interface","d3d12/ID3D12Resource::Unmap","direct3d12.id3d12resource_unmap"]
old-location: direct3d12\id3d12resource_unmap.htm
tech.root: direct3d12
ms.assetid: EB0E3936-47CC-4FDC-BF17-A506AC8E4C15
ms.date: 12/05/2018
ms.keywords: ID3D12Resource interface,Unmap method, ID3D12Resource.Unmap, ID3D12Resource::Unmap, Unmap, Unmap method, Unmap method,ID3D12Resource interface, d3d12/ID3D12Resource::Unmap, direct3d12.id3d12resource_unmap
req.header: d3d12.h
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Resource::Unmap
 - d3d12/ID3D12Resource::Unmap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Resource.Unmap
---

# ID3D12Resource::Unmap


## -description

Invalidates the CPU pointer to the specified subresource in the resource.

## -parameters

### -param Subresource

Type: <b>UINT</b>

Specifies the index of the subresource.

### -param pWrittenRange [in, optional]

Type: <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_range">D3D12_RANGE</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_range">D3D12_RANGE</a> structure that describes the range of memory to unmap.

This indicates the region the CPU might have modified, and the coordinates are subresource-relative. A null pointer indicates the entire subresource might have been modified by the CPU. It is valid to specify the CPU didn't write any data by passing a range where <b>End</b> is less than or equal to <b>Begin</b>.

This parameter is only used by tooling, and not for correctness of the actual unmap operation.

## -remarks

Refer to the extensive Remarks and Examples for the <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map">Map</a> method.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>



<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map">Map</a>



<a href="/windows/desktop/direct3d12/subresources">Subresources</a>
