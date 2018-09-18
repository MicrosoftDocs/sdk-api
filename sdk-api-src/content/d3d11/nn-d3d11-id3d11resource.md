---
UID: NN:d3d11.ID3D11Resource
title: ID3D11Resource
author: windows-sdk-content
description: A resource interface provides common actions on all resources.
old-location: direct3d11\id3d11resource.htm
tech.root: direct3d11
ms.assetid: 3823ec00-cb3c-43ce-9f1a-be4e1e99d587
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ID3D11Resource, ID3D11Resource interface [Direct3D 11], ID3D11Resource interface [Direct3D 11],described, d3d11/ID3D11Resource, d8e977b3-ff67-b931-bf00-8a95c24e06b7, direct3d11.id3d11resource
ms.prod: windows
ms.technology: windows-sdk
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Resource</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Ff476380(v=VS.85).aspx">ID3D11DeviceChild</a>. <b>ID3D11Resource</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Ff476585(v=VS.85).aspx">GetEvictionPriority</a>
</td>
<td align="left" width="63%">
Get the eviction priority of a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476586(v=VS.85).aspx">GetType</a>
</td>
<td align="left" width="63%">
Get the type of the resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476587(v=VS.85).aspx">SetEvictionPriority</a>
</td>
<td align="left" width="63%">
Set the eviction priority of a resource.

</td>
</tr>
</table> 


## -remarks



You don't directly create a resource interface; instead, you create buffers and textures that inherit from a resource interface. For more info,  see <a href="https://msdn.microsoft.com/en-us/library/Ff476899(v=VS.85).aspx">How to: Create a Vertex Buffer</a>, <a href="https://msdn.microsoft.com/en-us/library/Ff476897(v=VS.85).aspx">How to: Create an Index Buffer</a>, <a href="https://msdn.microsoft.com/en-us/library/Ff476896(v=VS.85).aspx">How to: Create a Constant Buffer</a>, and <a href="https://msdn.microsoft.com/en-us/library/Ff476903(v=VS.85).aspx">How to: Create a Texture</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476380(v=VS.85).aspx">ID3D11DeviceChild</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476172(v=VS.85).aspx">Resource Interfaces</a>
 

 

