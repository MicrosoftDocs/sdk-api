---
UID: NF:d3d10.ID3D10Resource.GetEvictionPriority
title: ID3D10Resource::GetEvictionPriority
author: windows-sdk-content
description: Get the eviction priority of a resource.
old-location: direct3d10\id3d10resource_getevictionpriority.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10resource_getevictionpriority.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 83f59a92-75b3-4efe-03ec-ca8afea155dc, GetEvictionPriority, GetEvictionPriority method [Direct3D 10], GetEvictionPriority method [Direct3D 10],ID3D10Resource interface, ID3D10Resource interface [Direct3D 10],GetEvictionPriority method, ID3D10Resource.GetEvictionPriority, ID3D10Resource::GetEvictionPriority, d3d10/ID3D10Resource::GetEvictionPriority, direct3d10.id3d10resource_getevictionpriority
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Resource::GetEvictionPriority


## -description


Get the eviction priority of a resource.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

One of the following values, which specifies the eviction priority for the resource:

<ul>
<li>DXGI_RESOURCE_PRIORITY_MINIMUM</li>
<li>DXGI_RESOURCE_PRIORITY_LOW</li>
<li>DXGI_RESOURCE_PRIORITY_NORMAL</li>
<li>DXGI_RESOURCE_PRIORITY_HIGH</li>
<li>DXGI_RESOURCE_PRIORITY_MAXIMUM</li>
</ul>



## -remarks



This method is a wrapper for <a href="https://msdn.microsoft.com/en-us/library/Bb174561(v=VS.85).aspx">GetEvictionPriority</a> and is provided in the <a href="https://msdn.microsoft.com/en-us/library/Bb173829(v=VS.85).aspx">ID3D10Resource Interface</a> interface for convenience.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173829(v=VS.85).aspx">ID3D10Resource Interface</a>
 

 

