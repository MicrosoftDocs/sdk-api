---
UID: NF:d3d11.ID3D11Resource.GetEvictionPriority
title: ID3D11Resource::GetEvictionPriority
author: windows-sdk-content
description: Get the eviction priority of a resource.
old-location: direct3d11\id3d11resource_getevictionpriority.htm
old-project: direct3d11
ms.assetid: 2ea8607a-56c1-4c1d-8c09-d16f9d3d914d
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: 6697dbf5-60e9-3ccc-6423-5ef98be8d001, GetEvictionPriority, GetEvictionPriority method [Direct3D 11], GetEvictionPriority method [Direct3D 11],ID3D11Resource interface, ID3D11Resource interface [Direct3D 11],GetEvictionPriority method, ID3D11Resource.GetEvictionPriority, ID3D11Resource::GetEvictionPriority, d3d11/ID3D11Resource::GetEvictionPriority, direct3d11.id3d11resource_getevictionpriority
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: D3D11_VPOV_DIMENSION
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
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Resource::GetEvictionPriority


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



## -see-also




<a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>
 

 

