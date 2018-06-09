---
UID: NF:dxgi.IDXGISurface.GetDesc
title: IDXGISurface::GetDesc
author: windows-sdk-content
description: Get a description of the surface.
old-location: direct3ddxgi\idxgisurface_getdesc.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgisurface_getdesc.htm
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: 92b3b49a-8f1d-7cd5-e484-3b5621c5acf5, GetDesc, GetDesc method [DXGI], GetDesc method [DXGI],IDXGISurface interface, IDXGISurface interface [DXGI],GetDesc method, IDXGISurface.GetDesc, IDXGISurface::GetDesc, direct3ddxgi.idxgisurface_getdesc, dxgi/IDXGISurface::GetDesc
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
 - IDXGISurface.GetDesc
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGISurface::GetDesc


## -description


Get a description of the surface.


## -parameters




### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/32c92c39-92bd-4d75-bd89-3e8a4ec093ab">DXGI_SURFACE_DESC</a>*</b>

A pointer to the surface description (see <a href="https://msdn.microsoft.com/32c92c39-92bd-4d75-bd89-3e8a4ec093ab">DXGI_SURFACE_DESC</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the error codes that are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic.




## -see-also




<a href="https://msdn.microsoft.com/9210b966-9e9a-4cd1-ba70-6f1a9fda9d80">IDXGISurface</a>
 

 

