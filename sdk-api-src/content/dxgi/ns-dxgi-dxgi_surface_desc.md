---
UID: NS:dxgi.DXGI_SURFACE_DESC
title: DXGI_SURFACE_DESC
author: windows-sdk-content
description: Describes a surface.
old-location: direct3ddxgi\dxgi_surface_desc.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\dxgi_surface_desc.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: 93817f74-4e10-480f-7425-b90c4fe26c0d, DXGI_SURFACE_DESC, DXGI_SURFACE_DESC structure [DXGI], direct3ddxgi.dxgi_surface_desc, dxgi/DXGI_SURFACE_DESC
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: DXGI_SURFACE_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI.h
api_name:
 - DXGI_SURFACE_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DXGI_SURFACE_DESC structure


## -description


Describes a surface.


## -struct-fields




### -field Width

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A value describing the surface width.


### -field Height

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A value describing the surface height.


### -field Format

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a></b>

A member of the <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a> enumerated type that describes the surface format.


### -field SampleDesc

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173072(v=VS.85).aspx">DXGI_SAMPLE_DESC</a></b>

A member of the <a href="https://msdn.microsoft.com/en-us/library/Bb173072(v=VS.85).aspx">DXGI_SAMPLE_DESC</a> structure that describes multi-sampling parameters for the surface.


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/en-us/library/Bb174566(v=VS.85).aspx">GetDesc</a> and  <a href="https://msdn.microsoft.com/library/windows/hardware/hh998978">CreateSurface</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>
 

 

