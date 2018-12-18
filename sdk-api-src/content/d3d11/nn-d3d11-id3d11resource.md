---
UID: NN:d3d11.ID3D11Resource
title: ID3D11Resource
author: windows-sdk-content
description: A resource interface provides common actions on all resources.
old-location: direct3d11\id3d11resource.htm
tech.root: direct3d11
ms.assetid: 3823ec00-cb3c-43ce-9f1a-be4e1e99d587
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D11Resource, ID3D11Resource interface [Direct3D 11], ID3D11Resource interface [Direct3D 11],described, d3d11/ID3D11Resource, d8e977b3-ff67-b931-bf00-8a95c24e06b7, direct3d11.id3d11resource
ms.topic: interface
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Resource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Resource interface


## -description


A resource interface provides common actions on all resources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Resource</b> interface inherits from <a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>. <b>ID3D11Resource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11Resource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ea8607a-56c1-4c1d-8c09-d16f9d3d914d">GetEvictionPriority</a>
</td>
<td align="left" width="63%">
Get the eviction priority of a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8358ab9b-acf3-41cd-8812-cc15862928da">GetType</a>
</td>
<td align="left" width="63%">
Get the type of the resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c68fbb8-dd8a-4d60-b081-082720e7bda5">SetEvictionPriority</a>
</td>
<td align="left" width="63%">
Set the eviction priority of a resource.

</td>
</tr>
</table> 


## -remarks



You don't directly create a resource interface; instead, you create buffers and textures that inherit from a resource interface. For more info,  see <a href="https://msdn.microsoft.com/584a39d1-7629-429a-b451-64b1432cb48f">How to: Create a Vertex Buffer</a>, <a href="https://msdn.microsoft.com/4b33d32a-27fd-4652-87ac-3b7268881f89">How to: Create an Index Buffer</a>, <a href="https://msdn.microsoft.com/78694ac2-e850-402d-8c99-6afb0bd5d660">How to: Create a Constant Buffer</a>, and <a href="https://msdn.microsoft.com/dfe88635-b2c2-48f8-a21e-cce845b518fc">How to: Create a Texture</a>.




## -see-also




<a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>



<a href="https://msdn.microsoft.com/8e40573a-b186-41ec-b2ff-81279d77bd3a">Resource Interfaces</a>
 

 

