---
UID: NF:dxgi.IDXGISurface.GetDesc
title: IDXGISurface::GetDesc
author: windows-sdk-content
description: Get a description of the surface.
old-location: direct3ddxgi\idxgisurface_getdesc.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgisurface_getdesc.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 92b3b49a-8f1d-7cd5-e484-3b5621c5acf5, GetDesc, GetDesc method [DXGI], GetDesc method [DXGI],IDXGISurface interface, IDXGISurface interface [DXGI],GetDesc method, IDXGISurface.GetDesc, IDXGISurface::GetDesc, direct3ddxgi.idxgisurface_getdesc, dxgi/IDXGISurface::GetDesc
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
 - IDXGISurface.GetDesc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGISurface::GetDesc


## -description


Get a description of the surface.


## -parameters




### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173074(v=VS.85).aspx">DXGI_SURFACE_DESC</a>*</b>

A pointer to the surface description (see <a href="https://msdn.microsoft.com/en-us/library/Bb173074(v=VS.85).aspx">DXGI_SURFACE_DESC</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the error codes that are described in the <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a> topic.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174565(v=VS.85).aspx">IDXGISurface</a>
 

 

