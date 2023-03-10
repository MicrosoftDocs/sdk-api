---
UID: NF:d3d10.ID3D10Resource.GetEvictionPriority
title: ID3D10Resource::GetEvictionPriority (d3d10.h)
description: Get the eviction priority of a resource. (ID3D10Resource.GetEvictionPriority)
helpviewer_keywords: ["83f59a92-75b3-4efe-03ec-ca8afea155dc","GetEvictionPriority","GetEvictionPriority method [Direct3D 10]","GetEvictionPriority method [Direct3D 10]","ID3D10Resource interface","ID3D10Resource interface [Direct3D 10]","GetEvictionPriority method","ID3D10Resource.GetEvictionPriority","ID3D10Resource::GetEvictionPriority","d3d10/ID3D10Resource::GetEvictionPriority","direct3d10.id3d10resource_getevictionpriority"]
old-location: direct3d10\id3d10resource_getevictionpriority.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10resource_getevictionpriority.htm
ms.date: 12/05/2018
ms.keywords: 83f59a92-75b3-4efe-03ec-ca8afea155dc, GetEvictionPriority, GetEvictionPriority method [Direct3D 10], GetEvictionPriority method [Direct3D 10],ID3D10Resource interface, ID3D10Resource interface [Direct3D 10],GetEvictionPriority method, ID3D10Resource.GetEvictionPriority, ID3D10Resource::GetEvictionPriority, d3d10/ID3D10Resource::GetEvictionPriority, direct3d10.id3d10resource_getevictionpriority
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Resource::GetEvictionPriority
 - d3d10/ID3D10Resource::GetEvictionPriority
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Resource.GetEvictionPriority
---

# ID3D10Resource::GetEvictionPriority


## -description

Get the eviction priority of a resource.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

One of the following values, which specifies the eviction priority for the resource:

<ul>
<li>DXGI_RESOURCE_PRIORITY_MINIMUM</li>
<li>DXGI_RESOURCE_PRIORITY_LOW</li>
<li>DXGI_RESOURCE_PRIORITY_NORMAL</li>
<li>DXGI_RESOURCE_PRIORITY_HIGH</li>
<li>DXGI_RESOURCE_PRIORITY_MAXIMUM</li>
</ul>

## -remarks

This method is a wrapper for <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getevictionpriority">GetEvictionPriority</a> and is provided in the <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource Interface</a> interface for convenience.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource Interface</a>
