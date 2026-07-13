---
UID: NF:d3d11.ID3D11Resource.SetEvictionPriority
title: ID3D11Resource::SetEvictionPriority (d3d11.h)
description: Set the eviction priority of a resource. (ID3D11Resource.SetEvictionPriority)
helpviewer_keywords: ["55340049-7283-9bea-b4ac-8b0b9cb71119","ID3D11Resource interface [Direct3D 11]","SetEvictionPriority method","ID3D11Resource.SetEvictionPriority","ID3D11Resource::SetEvictionPriority","SetEvictionPriority","SetEvictionPriority method [Direct3D 11]","SetEvictionPriority method [Direct3D 11]","ID3D11Resource interface","d3d11/ID3D11Resource::SetEvictionPriority","direct3d11.id3d11resource_setevictionpriority"]
old-location: direct3d11\id3d11resource_setevictionpriority.htm
tech.root: direct3d11
ms.assetid: 8c68fbb8-dd8a-4d60-b081-082720e7bda5
ms.date: 12/05/2018
ms.keywords: 55340049-7283-9bea-b4ac-8b0b9cb71119, ID3D11Resource interface [Direct3D 11],SetEvictionPriority method, ID3D11Resource.SetEvictionPriority, ID3D11Resource::SetEvictionPriority, SetEvictionPriority, SetEvictionPriority method [Direct3D 11], SetEvictionPriority method [Direct3D 11],ID3D11Resource interface, d3d11/ID3D11Resource::SetEvictionPriority, direct3d11.id3d11resource_setevictionpriority
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
 - ID3D11Resource::SetEvictionPriority
 - d3d11/ID3D11Resource::SetEvictionPriority
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
 - ID3D11Resource.SetEvictionPriority
---

# ID3D11Resource::SetEvictionPriority


## -description

Set the eviction priority of a resource.

## -parameters

### -param EvictionPriority [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Eviction priority for the resource, which is one of the following values:

<ul>
<li>DXGI_RESOURCE_PRIORITY_MINIMUM</li>
<li>DXGI_RESOURCE_PRIORITY_LOW</li>
<li>DXGI_RESOURCE_PRIORITY_NORMAL</li>
<li>DXGI_RESOURCE_PRIORITY_HIGH</li>
<li>DXGI_RESOURCE_PRIORITY_MAXIMUM</li>
</ul>

## -remarks

Resource priorities determine which resource to evict from video memory when the system has run out of video memory. The resource will not be lost; it will be removed from video memory and placed into system memory, or possibly placed onto the hard drive. The resource will be loaded back into video memory when it is required.

A resource that is set to the maximum priority, DXGI_RESOURCE_PRIORITY_MAXIMUM, is only evicted if there is no other way of resolving the incoming memory request. The Windows Display Driver Model (WDDM) tries to split an incoming memory request to its minimum size and evict lower-priority resources before evicting a resource with maximum priority.

Changing the priorities of resources should be done carefully. The wrong eviction priorities could be a detriment to performance rather than an improvement.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>
