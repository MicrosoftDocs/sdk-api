---
UID: NF:d3d11.ID3D11Resource.GetEvictionPriority
title: ID3D11Resource::GetEvictionPriority (d3d11.h)
description: Get the eviction priority of a resource. (ID3D11Resource.GetEvictionPriority)
helpviewer_keywords: ["6697dbf5-60e9-3ccc-6423-5ef98be8d001","GetEvictionPriority","GetEvictionPriority method [Direct3D 11]","GetEvictionPriority method [Direct3D 11]","ID3D11Resource interface","ID3D11Resource interface [Direct3D 11]","GetEvictionPriority method","ID3D11Resource.GetEvictionPriority","ID3D11Resource::GetEvictionPriority","d3d11/ID3D11Resource::GetEvictionPriority","direct3d11.id3d11resource_getevictionpriority"]
old-location: direct3d11\id3d11resource_getevictionpriority.htm
tech.root: direct3d11
ms.assetid: 2ea8607a-56c1-4c1d-8c09-d16f9d3d914d
ms.date: 12/05/2018
ms.keywords: 6697dbf5-60e9-3ccc-6423-5ef98be8d001, GetEvictionPriority, GetEvictionPriority method [Direct3D 11], GetEvictionPriority method [Direct3D 11],ID3D11Resource interface, ID3D11Resource interface [Direct3D 11],GetEvictionPriority method, ID3D11Resource.GetEvictionPriority, ID3D11Resource::GetEvictionPriority, d3d11/ID3D11Resource::GetEvictionPriority, direct3d11.id3d11resource_getevictionpriority
req.header: d3d11.h
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
 - ID3D11Resource::GetEvictionPriority
 - d3d11/ID3D11Resource::GetEvictionPriority
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
 - ID3D11Resource.GetEvictionPriority
---

# ID3D11Resource::GetEvictionPriority


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

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>
