---
UID: NN:d3d10.ID3D10Resource
title: ID3D10Resource
author: windows-sdk-content
description: A resource interface provides common actions on all resources.
old-location: direct3d10\id3d10resource.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10resource.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ID3D10Resource, ID3D10Resource interface [Direct3D 10], ID3D10Resource interface [Direct3D 10],described, a827797e-b4b8-c82b-c567-463061c6d963, d3d10/ID3D10Resource, direct3d10.id3d10resource
ms.prod: windows
ms.technology: windows-sdk
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
 - ID3D10Resource
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Resource interface


## -description


A resource interface provides common actions on all <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">resources</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Resource</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb173529(v=VS.85).aspx">ID3D10DeviceChild</a>. <b>ID3D10Resource</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Bb173830(v=VS.85).aspx">GetEvictionPriority</a>
</td>
<td align="left" width="63%">
Get the eviction priority of a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991813">GetType</a>
</td>
<td align="left" width="63%">
Get the type of the resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173832(v=VS.85).aspx">SetEvictionPriority</a>
</td>
<td align="left" width="63%">
Set the eviction priority of a resource.

</td>
</tr>
</table> 


## -remarks



A resource interface cannot be created directly; instead, <a href="https://msdn.microsoft.com/library/windows/hardware/dn938497">buffers</a> and textures are created that inherit from a resource interface (see <a href="https://msdn.microsoft.com/en-us/library/Bb205130(v=VS.85).aspx">Creating Buffer Resources</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb205131(v=VS.85).aspx">Creating Texture Resources</a>).




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173529(v=VS.85).aspx">ID3D10DeviceChild</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb205276(v=VS.85).aspx">Resource Interfaces</a>
 

 

