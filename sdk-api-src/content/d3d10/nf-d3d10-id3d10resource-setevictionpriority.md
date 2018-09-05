---
UID: NF:d3d10.ID3D10Resource.SetEvictionPriority
title: ID3D10Resource::SetEvictionPriority
author: windows-sdk-content
description: Set the eviction priority of a resource.
old-location: direct3d10\id3d10resource_setevictionpriority.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10resource_setevictionpriority.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: 8ad141ef-5f50-f2f6-d2db-3f0b076d0dda, ID3D10Resource interface [Direct3D 10],SetEvictionPriority method, ID3D10Resource.SetEvictionPriority, ID3D10Resource::SetEvictionPriority, SetEvictionPriority, SetEvictionPriority method [Direct3D 10], SetEvictionPriority method [Direct3D 10],ID3D10Resource interface, d3d10/ID3D10Resource::SetEvictionPriority, direct3d10.id3d10resource_setevictionpriority
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Resource.SetEvictionPriority
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Resource::SetEvictionPriority


## -description


Set the eviction priority of a resource.


## -parameters




### -param EvictionPriority [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Eviction priority for the resource, which is one of the following values:

<ul>
<li>DXGI_RESOURCE_PRIORITY_MINIMUM</li>
<li>DXGI_RESOURCE_PRIORITY_LOW</li>
<li>DXGI_RESOURCE_PRIORITY_NORMAL</li>
<li>DXGI_RESOURCE_PRIORITY_HIGH</li>
<li>DXGI_RESOURCE_PRIORITY_MAXIMUM</li>
</ul>

## -returns



Returns nothing.




## -remarks



Resource priorities determine which resource to evict from video memory when the system has run out of video memory. The resource will not be lost; it will be removed from video memory and placed into system memory, or possibly placed onto the hard drive. The resource will be loaded back into video memory when it is required.

A resource that is set to the maximum priority, DXGI_RESOURCE_PRIORITY_MAXIMUM, is only evicted if there is no other way of resolving the incoming memory request. The Windows Display Driver Model (WDDM) tries to split an incoming memory request to its minimum size and evict lower-priority resources before evicting a resource with maximum priority.

Changing the priorities of resources should be done carefully. The wrong eviction priorities could be a detriment to performance rather than an improvement. See <a href="https://msdn.microsoft.com/a03af142-657b-459d-abba-fdee72e77db9">QueryResourceResidency</a> for additional information.

This method is a wrapper for <a href="https://msdn.microsoft.com/ed9417ee-8074-4022-bce9-230fec1c7093">SetEvictionPriority</a> and is provided in the <a href="https://msdn.microsoft.com/709c6f33-e1dc-4609-8ddd-9dc502628ec5">ID3D10Resource Interface</a> interface for convenience.




## -see-also




<a href="https://msdn.microsoft.com/709c6f33-e1dc-4609-8ddd-9dc502628ec5">ID3D10Resource Interface</a>
 

 

