---
UID: NF:gdiplusheaders.Region.IsVisible(IN const RectF &,IN const Graphics)
title: Region::IsVisible(IN const RectF &,IN const Graphics) (gdiplusheaders.h)
author: windows-sdk-content
description: The Region::IsVisible method determines whether a rectangle intersects this region.
old-location: gdiplus\_gdiplus_CLASS_Region_IsVisible_RectF_rect_Graphics_g_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\regionisvisiblemethods\isvisible_24rectfamprect_graphicsg.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IsVisible, IsVisible method [GDI+], IsVisible method [GDI+],Region class, Region class [GDI+],IsVisible method, Region.IsVisible, Region.IsVisible(IN const RectF &,IN const Graphics), Region.IsVisible(const RectF&,const Graphics*), Region::IsVisible, Region::IsVisible(IN const RectF &,IN const Graphics), _gdiplus_CLASS_Region_IsVisible_RectF_rect_Graphics_g_, gdiplus._gdiplus_CLASS_Region_IsVisible_RectF_rect_Graphics_g_
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
 - Region.IsVisible
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Region::IsVisible(IN const RectF &,IN const Graphics)


## -description


The <b>Region::IsVisible</b> method determines whether a rectangle intersects this region.


## -parameters




### -param rect [in, ref]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a></b>

Reference to a rectangle to test. 


### -param g [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>*</b>

Optional. Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object that contains the world and page transformations required to calculate the device coordinates of this region and the rectangle. The default value is <b>NULL</b>. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the rectangle intersects this region, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -remarks



<div class="alert"><b>Note</b>  A region contains its border.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>
 

 

