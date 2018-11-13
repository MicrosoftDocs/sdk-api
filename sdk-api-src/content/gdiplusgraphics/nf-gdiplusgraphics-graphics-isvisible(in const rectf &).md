---
UID: NF:gdiplusgraphics.Graphics.IsVisible(IN const RectF &)
title: Graphics::IsVisible(IN const RectF &)
author: windows-sdk-content
description: The Graphics::IsVisible method determines whether the specified rectangle intersects the visible clipping region of this Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_IsVisible_RectF_rect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsisvisiblemethods\isvisible_15rectfamprect.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: Graphics class [GDI+],IsVisible method, Graphics.IsVisible, Graphics.IsVisible(IN const RectF &), Graphics.IsVisible(const RectF&), Graphics::IsVisible, Graphics::IsVisible(IN const RectF &), IsVisible, IsVisible method [GDI+], IsVisible method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_IsVisible_RectF_rect_, gdiplus._gdiplus_CLASS_Graphics_IsVisible_RectF_rect_
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
 - Graphics.IsVisible
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::IsVisible(IN const RectF &)


## -description


The <b>Graphics::IsVisible</b> method determines whether the specified rectangle intersects the visible clipping region of this <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object. The visible clipping region is the intersection of the clipping region of this <b>Graphics</b> object and the clipping region of the window.


## -parameters




### -param rect [in]

Type: <b>const RectF&amp;</b>

Reference to a rectangle to be tested to see whether it intersects the visible clipping region. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the specified rectangle intersects the visible clipping region, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/73733baf-6cbf-4220-b89d-0cd6856acc46">Graphics::IsVisibleClipEmpty</a>



<a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a>
 

 

