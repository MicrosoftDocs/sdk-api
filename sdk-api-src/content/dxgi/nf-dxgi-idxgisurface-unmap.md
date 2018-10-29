---
UID: NF:dxgi.IDXGISurface.Unmap
title: IDXGISurface::Unmap
author: windows-sdk-content
description: Invalidate the pointer to the surface retrieved by IDXGISurface::Map and re-enable GPU access to the resource.
old-location: direct3ddxgi\idxgisurface_unmap.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgisurface_unmap.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 72e0302e-2a02-c42b-8a5c-609c0e5f562a, IDXGISurface interface [DXGI],Unmap method, IDXGISurface.Unmap, IDXGISurface::Unmap, Unmap, Unmap method [DXGI], Unmap method [DXGI],IDXGISurface interface, direct3ddxgi.idxgisurface_unmap, dxgi/IDXGISurface::Unmap
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: DXGI.lib
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
---

# IDXGISurface::Unmap


## -description


Invalidate the pointer to the surface retrieved by <a href="https://msdn.microsoft.com/027da15c-1670-41ec-a633-addd1c5ff150">IDXGISurface::Map</a> and re-enable GPU access to the resource.


## -parameters






## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the error codes that are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic.




## -see-also




<a href="https://msdn.microsoft.com/9210b966-9e9a-4cd1-ba70-6f1a9fda9d80">IDXGISurface</a>
 

 

