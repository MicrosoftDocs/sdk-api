---
UID: NF:gdiplusgraphics.Graphics.ExcludeClip(IN const Region)
title: Graphics::ExcludeClip(IN const Region)
author: windows-sdk-content
description: The Graphics::ExcludeClip method updates the clipping region with the portion of itself that does not overlap the specified region.
old-location: gdiplus\_gdiplus_CLASS_Graphics_ExcludeClip_region_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsexcludeclipmethods\excludeclip_98region.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ExcludeClip, ExcludeClip method [GDI+], ExcludeClip method [GDI+],Graphics class, Graphics class [GDI+],ExcludeClip method, Graphics.ExcludeClip, Graphics.ExcludeClip(IN const Region), Graphics.ExcludeClip(const Region*), Graphics::ExcludeClip, Graphics::ExcludeClip(IN const Region), _gdiplus_CLASS_Graphics_ExcludeClip_region_, gdiplus._gdiplus_CLASS_Graphics_ExcludeClip_region_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusgraphics.h
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
 - Graphics.ExcludeClip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::ExcludeClip(IN const Region)


## -description


The <b>Graphics::ExcludeClip</b> method updates the clipping region with the portion of itself that does not overlap the specified region.


## -parameters




### -param region [in]

Type: <b>const <a href="https://msdn.microsoft.com/2972b879-7d2f-4cad-b17d-670125f43691">Region</a>*</b>

Pointer to the region to use to update the clipping region. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>



<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a>
 

 

