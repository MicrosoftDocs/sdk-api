---
UID: NF:gdiplusgraphics.Graphics.IsVisible(IN const PointF &)
title: Graphics::IsVisible(IN const PointF &)
author: windows-sdk-content
description: The Graphics::IsVisible method determines whether the specified point is inside the visible clipping region of this Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_IsVisible_PointF_point_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsisvisiblemethods\isvisible_44pointfamppoint.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Graphics class [GDI+],IsVisible method, Graphics.IsVisible, Graphics.IsVisible(IN const PointF &), Graphics.IsVisible(const PointF&), Graphics::IsVisible, Graphics::IsVisible(IN const PointF &), IsVisible, IsVisible method [GDI+], IsVisible method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_IsVisible_PointF_point_, gdiplus._gdiplus_CLASS_Graphics_IsVisible_PointF_point_
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
- apiref
: 
- COM
: 
- gdiplusgraphics.h
: 
- Graphics.IsVisible
: 
req.product: GDI+ 1.0
---

# Graphics::IsVisible(IN const PointF &)


## -description


The <b>Graphics::IsVisible</b> method determines whether the specified point is inside the visible clipping region of this 
			<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object. The visible clipping region is the intersection of the clipping region of this 
			<b>Graphics</b> object and the clipping region of the window.


## -parameters




### -param point [in]

Type: <b>const PointF&amp;</b>

Reference to a point to be tested to see whether it is inside the visible clipping region. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the specified point is inside the visible clipping region, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/73733baf-6cbf-4220-b89d-0cd6856acc46">Graphics::IsVisibleClipEmpty</a>



<a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>
 

 

