---
UID: NF:gdiplusheaders.Region.Union(IN const Rect &)
title: Region::Union(IN const Rect &)
author: windows-sdk-content
description: The Region::Union method updates this region to all portions (intersecting and nonintersecting) of itself and all portions of the specified rectangle's interior.
old-location: gdiplus\_gdiplus_CLASS_Region_Union_Rect_rect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\regionunionmethods\union_21rectamprect.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Region class [GDI+],Union method, Region.Union, Region.Union(IN const Rect &), Region.Union(const Rect&), Region::Union, Region::Union(IN const Rect &), Union, Union method [GDI+], Union method [GDI+],Region class, _gdiplus_CLASS_Region_Union_Rect_rect_, gdiplus._gdiplus_CLASS_Region_Union_Rect_rect_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Region.Union
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdiplusheaders.h
: 
- Region.Union
: 
req.product: GDI+ 1.0
---

# Region::Union(IN const Rect &)


## -description


The <b>Region::Union</b> method updates this region to all portions (intersecting and nonintersecting) of itself and all portions of the specified rectangle's interior.


## -parameters




### -param rect [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a></b>

Reference to a rectangle to use to update this region. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>



<a href="https://msdn.microsoft.com/2972b879-7d2f-4cad-b17d-670125f43691">Region</a>



<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a>
 

 

