---
UID: NN:d3d10.ID3D10Resource
title: ID3D10Resource
author: windows-sdk-content
description: A resource interface provides common actions on all resources.
old-location: direct3d10\id3d10resource.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10resource.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D10Resource, ID3D10Resource interface [Direct3D 10], ID3D10Resource interface [Direct3D 10],described, a827797e-b4b8-c82b-c567-463061c6d963, d3d10/ID3D10Resource, direct3d10.id3d10resource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - ID3D10Resource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Resource interface


## -description


A resource interface provides common actions on all <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">resources</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Resource</b> interface inherits from <a href="https://msdn.microsoft.com/64eff938-e130-48be-a45f-43f6c885b588">ID3D10DeviceChild</a>. <b>ID3D10Resource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10Resource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47ed836a-c16f-4888-82f1-69070d6d7f4d">GetEvictionPriority</a>
</td>
<td align="left" width="63%">
Get the eviction priority of a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/78e91654-e3e7-4565-99be-8ccf480b954b">GetType</a>
</td>
<td align="left" width="63%">
Get the type of the resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1bc3354-4abe-4f7f-bf32-43025f34ed9e">SetEvictionPriority</a>
</td>
<td align="left" width="63%">
Set the eviction priority of a resource.

</td>
</tr>
</table> 


## -remarks



A resource interface cannot be created directly; instead, <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">buffers</a> and textures are created that inherit from a resource interface (see <a href="https://msdn.microsoft.com/9787b153-9301-4a0f-bd6f-21cc6f7fc650">Creating Buffer Resources</a> or <a href="https://msdn.microsoft.com/4c716be8-044e-4ed4-aeca-4379440826bd">Creating Texture Resources</a>).




## -see-also




<a href="https://msdn.microsoft.com/64eff938-e130-48be-a45f-43f6c885b588">ID3D10DeviceChild</a>



<a href="https://msdn.microsoft.com/e53ca7ab-6ca5-4774-8a52-825b10c1a2ce">Resource Interfaces</a>
 

 

