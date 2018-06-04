---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IDXGIResource1::CreateSubresourceSurface


## -description


Creates a subresource surface object.


## -parameters




### -param index

The index of the subresource surface object to enumerate.


### -param ppSurface [out]

The address of a pointer to a <a href="https://msdn.microsoft.com/EBBB2EE1-C5EA-4F98-AA8B-BCAA8C188F26">IDXGISurface2</a> interface that represents the created subresource surface object at the position specified by the <i>index</i> parameter.


## -returns



Returns S_OK if successful; otherwise, returns one of the following values:

<ul>
<li><a href="dxgi_error.htm">DXGI_ERROR_INVALID_CALL</a> if the index is out of range or if the subresource is not a valid surface.</li>
<li>E_OUTOFMEMORY if insufficient memory is available to create the subresource surface object.</li>
</ul>
A subresource is a valid surface if the original resource would have been a valid surface had its array size been equal to 1.




## -remarks



Subresource surface objects implement the <a href="https://msdn.microsoft.com/EBBB2EE1-C5EA-4F98-AA8B-BCAA8C188F26">IDXGISurface2</a> interface, which inherits from  <a href="https://msdn.microsoft.com/99ece4f3-1bad-46b8-94a9-6ef559864b1c">IDXGISurface1</a> and indirectly <a href="https://msdn.microsoft.com/9210b966-9e9a-4cd1-ba70-6f1a9fda9d80">IDXGISurface</a>.  Therefore, the GDI-interoperable methods of <b>IDXGISurface1</b> work if the original resource interface object was created with the GDI-interoperable flag (<a href="https://msdn.microsoft.com/2a324055-21b0-4dad-a8e0-781905329dc2">D3D11_RESOURCE_MISC_GDI_COMPATIBLE</a>).

<b>CreateSubresourceSurface</b> creates a subresource surface that is based on the resource interface on which <b>CreateSubresourceSurface</b> is called. For example, if the original resource interface object is a 2D texture, the created subresource surface is also a 2D texture.

You can use <b>CreateSubresourceSurface</b> to create parts of  a stereo resource so you can use Direct2D on either the left or right part of the stereo resource.




## -see-also




<a href="https://msdn.microsoft.com/0ABA9B8D-BEA4-4455-A312-7CFEDEBBF19A">IDXGIResource1</a>
 

 

