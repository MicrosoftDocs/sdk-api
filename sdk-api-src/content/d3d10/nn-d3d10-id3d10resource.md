---
UID: NN:d3d10.ID3D10Resource
title: ID3D10Resource (d3d10.h)

description: A resource interface provides common actions on all resources.
old-location: direct3d10\id3d10resource.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10resource.htm

ms.date: 12/05/2018
ms.keywords: ID3D10Resource, ID3D10Resource interface [Direct3D 10], ID3D10Resource interface [Direct3D 10],described, a827797e-b4b8-c82b-c567-463061c6d963, d3d10/ID3D10Resource, direct3d10.id3d10resource
ms.topic: interface
f1_keywords: 
 - "d3d10/ID3D10Resource"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10Resource interface


## -description


A resource interface provides common actions on all <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">resources</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Resource</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>. <b>ID3D10Resource</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10resource-getevictionpriority">GetEvictionPriority</a>
</td>
<td align="left" width="63%">
Get the eviction priority of a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10resource-gettype">GetType</a>
</td>
<td align="left" width="63%">
Get the type of the resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10resource-setevictionpriority">SetEvictionPriority</a>
</td>
<td align="left" width="63%">
Set the eviction priority of a resource.

</td>
</tr>
</table> 


## -remarks



A resource interface cannot be created directly; instead, <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">buffers</a> and textures are created that inherit from a resource interface (see <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating">Creating Buffer Resources</a> or <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating-textures">Creating Texture Resources</a>).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-resource-interfaces">Resource Interfaces</a>
 

 

