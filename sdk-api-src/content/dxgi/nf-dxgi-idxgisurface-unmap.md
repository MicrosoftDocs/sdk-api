---
UID: NF:dxgi.IDXGISurface.Unmap
title: IDXGISurface::Unmap
author: windows-sdk-content
description: Invalidate the pointer to the surface retrieved by IDXGISurface::Map and re-enable GPU access to the resource.
old-location: direct3ddxgi\idxgisurface_unmap.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgisurface_unmap.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: 72e0302e-2a02-c42b-8a5c-609c0e5f562a, IDXGISurface interface [DXGI],Unmap method, IDXGISurface.Unmap, IDXGISurface::Unmap, Unmap, Unmap method [DXGI], Unmap method [DXGI],IDXGISurface interface, direct3ddxgi.idxgisurface_unmap, dxgi/IDXGISurface::Unmap
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi.h
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
req.typenames: DXGI_SWAP_EFFECT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGISurface.Unmap
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGISurface::Unmap


## -description


Invalidate the pointer to the surface retrieved by <a href="https://msdn.microsoft.com/library/Bb174567(v=VS.85).aspx">IDXGISurface::Map</a> and re-enable GPU access to the resource.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the error codes that are described in the <a href="https://msdn.microsoft.com/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a> topic.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb174565(v=VS.85).aspx">IDXGISurface</a>
 

 

