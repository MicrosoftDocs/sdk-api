---
UID: NF:gdiplusgraphics.Graphics.ExcludeClip(IN const Region)
title: Graphics::ExcludeClip(IN const Region) (gdiplusgraphics.h)
description: The Graphics::ExcludeClip method updates the clipping region with the portion of itself that does not overlap the specified region.helpviewer_keywords: ["ExcludeClip","ExcludeClip method [GDI+]","ExcludeClip method [GDI+]","Graphics class","Graphics class [GDI+]","ExcludeClip method","Graphics.ExcludeClip","Graphics.ExcludeClip(IN const Region)","Graphics.ExcludeClip(const Region*)","Graphics::ExcludeClip","Graphics::ExcludeClip(IN const Region)","_gdiplus_CLASS_Graphics_ExcludeClip_region_","gdiplus._gdiplus_CLASS_Graphics_ExcludeClip_region_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_ExcludeClip_region_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsexcludeclipmethods\excludeclip_98region.htm
ms.date: 12/05/2018
ms.keywords: ExcludeClip, ExcludeClip method [GDI+], ExcludeClip method [GDI+],Graphics class, Graphics class [GDI+],ExcludeClip method, Graphics.ExcludeClip, Graphics.ExcludeClip(IN const Region), Graphics.ExcludeClip(const Region*), Graphics::ExcludeClip, Graphics::ExcludeClip(IN const Region), _gdiplus_CLASS_Graphics_ExcludeClip_region_, gdiplus._gdiplus_CLASS_Graphics_ExcludeClip_region_
f1_keywords:
- gdiplusgraphics/Graphics.ExcludeClip
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Graphics::ExcludeClip(IN const Region)


## -description


The <b>Graphics::ExcludeClip</b> method updates the clipping region with the portion of itself that does not overlap the specified region.


## -parameters




### -param region [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>*</b>

Pointer to the region to use to update the clipping region. 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>
 

 

