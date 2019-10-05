---
UID: NF:gdiplusgraphics.Graphics.SetClip(IN const Region,IN CombineMode)
title: Graphics::SetClip(IN const Region,IN CombineMode) (gdiplusgraphics.h)
author: windows-sdk-content
description: The Graphics::SetClip method updates the clipping region of this Graphics object to a region that is the combination of itself and the region specified by a Region object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetClip_region_combineMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicssetclipmethods\setclip_48region_combinemode.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],SetClip method, Graphics.SetClip, Graphics.SetClip(IN const Region,IN CombineMode), Graphics.SetClip(const Region*,CombineMode), Graphics::SetClip, Graphics::SetClip(IN const Region,IN CombineMode), SetClip, SetClip method [GDI+], SetClip method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_SetClip_region_combineMode_, gdiplus._gdiplus_CLASS_Graphics_SetClip_region_combineMode_
ms.topic: method
f1_keywords: 
 - "gdiplusgraphics/Graphics.SetClip"
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
 - Graphics.SetClip
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Graphics::SetClip(IN const Region,IN CombineMode)


## -description


The <b>Graphics::SetClip</b> method updates the clipping region of this <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object to a region that is the combination of itself and the region specified by a <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a> object.


## -parameters




### -param region [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a> object that specifies the region to be combined with the clipping region of this <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object. 


### -param combineMode [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-combinemode">CombineMode</a></b>

Optional. Element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-combinemode">CombineMode</a> enumeration that specifies how the specified region is combined with the clipping region of this <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object. The default value is CombineModeReplace. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-clipping-about">Clipping</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-combinemode">CombineMode</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getclipbounds(outrect)">GetClipBounds Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getclip">Graphics::GetClip</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-isclipempty">Graphics::IsClipEmpty</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-resetclip">Graphics::ResetClip</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-intersectclip(inconstrect_)">IntersectClip Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-translateclip(inint_inint)">TranslateClip Methods</a>
 

 

