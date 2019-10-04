---
UID: NS:dxgi.DXGI_MAPPED_RECT
title: DXGI_MAPPED_RECT (dxgi.h)
author: windows-sdk-content
description: Describes a mapped rectangle that is used to access a surface.
old-location: direct3ddxgi\dxgi_mapped_rect.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\dxgi_mapped_rect.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 44004772-851a-9ebf-10ab-60178c7e35c5, DXGI_MAPPED_RECT, DXGI_MAPPED_RECT structure [DXGI], direct3ddxgi.dxgi_mapped_rect, dxgi/DXGI_MAPPED_RECT
ms.topic: struct
f1_keywords: 
 - "dxgi/DXGI_MAPPED_RECT"
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI.h
api_name:
 - DXGI_MAPPED_RECT
targetos: Windows
req.typenames: DXGI_MAPPED_RECT
req.redist: 
ms.custom: 19H1
---

# DXGI_MAPPED_RECT structure


## -description


Describes a mapped rectangle that is used to access a surface.


## -struct-fields




### -field Pitch

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">INT</a></b>

A value that describes the width, in bytes, of the surface.


### -field pBits

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BYTE</a>*</b>

A pointer to the image buffer of the surface.


## -remarks



The <b>DXGI_MAPPED_RECT</b> structure is initialized by the <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgisurface-map">IDXGISurface::Map</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>
 

 

