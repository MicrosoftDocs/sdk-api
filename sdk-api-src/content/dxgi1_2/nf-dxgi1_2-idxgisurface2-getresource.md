---
UID: NF:dxgi1_2.IDXGISurface2.GetResource
title: IDXGISurface2::GetResource
author: windows-sdk-content
description: Gets the parent resource and subresource index that support a subresource surface.
old-location: direct3ddxgi\idxgisurface2_getresource.htm
tech.root: direct3ddxgi
ms.assetid: 0CDA5693-610F-4E7E-9540-353709E4FA8D
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetResource, GetResource method [DXGI], GetResource method [DXGI],IDXGISurface2 interface, IDXGISurface2 interface [DXGI],GetResource method, IDXGISurface2.GetResource, IDXGISurface2::GetResource, direct3ddxgi.idxgisurface2_getresource, dxgi1_2/IDXGISurface2::GetResource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxgi.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGISurface2.GetResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dxgi1_2.h
: 
- IDXGISurface2.GetResource
: 
---

# IDXGISurface2::GetResource


## -description


Gets the parent resource and subresource index that support a subresource surface.


## -parameters




### -param riid [in]

The globally unique identifier (GUID)  of the requested interface type.


### -param ppParentResource [out]

A pointer to a buffer that receives a pointer to the parent resource object for the subresource surface.


### -param pSubresourceIndex [out]

A pointer to a variable that receives the index of the subresource surface.


## -returns



Returns S_OK if successful; otherwise, returns one of the following values:

<ul>
<li>E_NOINTERFACE if the object does not implement the GUID that the <i>riid</i> parameter specifies.</li>
<li>Possibly other error codes that are described in the <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a> topic.</li>
</ul>



## -remarks



For subresource surface objects that the <a href="https://msdn.microsoft.com/99730AB1-C5D9-41D6-8001-495FF26E8232">IDXGIResource1::CreateSubresourceSurface</a> method creates, <b>GetResource</b> simply returns the values that were used to create the subresource surface.

Current objects that implement <a href="https://msdn.microsoft.com/en-us/library/Bb174565(v=VS.85).aspx">IDXGISurface</a> are either resources or views.  <b>GetResource</b> for these objects returns “this” or the resource that supports the view respectively.  In this situation, the subresource index is 0.




## -see-also




<a href="https://msdn.microsoft.com/EBBB2EE1-C5EA-4F98-AA8B-BCAA8C188F26">IDXGISurface2</a>
 

 

