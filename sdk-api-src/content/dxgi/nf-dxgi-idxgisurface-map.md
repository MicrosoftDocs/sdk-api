---
UID: NF:dxgi.IDXGISurface.Map
title: IDXGISurface::Map
author: windows-sdk-content
description: Get a pointer to the data contained in the surface, and deny GPU access to the surface.
old-location: direct3ddxgi\idxgisurface_map.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgisurface_map.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: 2353661a-8e73-6878-2899-79d0afdc2901, IDXGISurface interface [DXGI],Map method, IDXGISurface.Map, IDXGISurface::Map, Map, Map method [DXGI], Map method [DXGI],IDXGISurface interface, direct3ddxgi.idxgisurface_map, dxgi/IDXGISurface::Map
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi.h
req.include-header: 
req.redist: 
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
 - IDXGISurface.Map
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGISurface::Map


## -description


Get a pointer to the data contained in the surface, and deny GPU access to the surface.


## -parameters




### -param pLockedRect [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173063(v=VS.85).aspx">DXGI_MAPPED_RECT</a>*</b>

A pointer to the surface data (see <a href="https://msdn.microsoft.com/en-us/library/Bb173063(v=VS.85).aspx">DXGI_MAPPED_RECT</a>).


### -param MapFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

CPU read-write flags. These flags can be combined with a logical OR.



<ul>
<li>DXGI_MAP_READ - Allow CPU read access.</li>
<li>DXGI_MAP_WRITE - Allow CPU write access.</li>
<li>DXGI_MAP_DISCARD - Discard the previous contents of a resource when it is mapped.</li>
</ul>

## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the error codes that are described in the <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a> topic.




## -remarks



Use <b>IDXGISurface::Map</b> to access a surface from the CPU. To release a mapped surface (and allow GPU access) call <a href="https://msdn.microsoft.com/en-us/library/Bb174568(v=VS.85).aspx">IDXGISurface::Unmap</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174565(v=VS.85).aspx">IDXGISurface</a>
 

 

