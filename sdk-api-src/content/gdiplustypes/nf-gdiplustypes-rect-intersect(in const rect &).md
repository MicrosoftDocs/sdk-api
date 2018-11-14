---
UID: NF:gdiplustypes.Rect.Intersect(IN const Rect &)
title: Rect::Intersect(IN const Rect &)
author: windows-sdk-content
description: The Rect::Intersect method replaces this rectangle with the intersection of itself and another rectangle.
old-location: gdiplus\_gdiplus_CLASS_Rect_Intersect_rect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\rectclass\rectmethods\rectintersectmethods\intersect_7rect.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: Intersect, Intersect method [GDI+], Intersect method [GDI+],Rect class, Rect class [GDI+],Intersect method, Rect.Intersect, Rect.Intersect(IN const Rect &), Rect.Intersect(const Rect&), Rect::Intersect, Rect::Intersect(IN const Rect &), _gdiplus_CLASS_Rect_Intersect_rect_, gdiplus._gdiplus_CLASS_Rect_Intersect_rect_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplustypes.h
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
 - Rect.Intersect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdiplustypes.h
: 
- Rect.Intersect
: 
req.product: GDI+ 1.0
---

# Rect::Intersect(IN const Rect &)


## -description


The <b>Rect::Intersect</b> method replaces this rectangle with the intersection of itself and another rectangle.


## -parameters




### -param rect [in]

Type: <b>const Rect&amp;</b>

Reference to a rectangle to intersect with this rectangle. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the intersection of the two rectangles is not empty, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/b391c256-5165-4c5c-a45a-dee74e32d391">Intersect Methods</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>



<a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a>



<a href="https://msdn.microsoft.com/f2e4144f-f2f1-49db-bfdf-ffce3023b4cb">Using a Pen to Draw Lines and Rectangles</a>
 

 

