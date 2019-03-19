---
UID: NF:gdiplustypes.RectF.Intersect(OUT RectF &,IN const RectF &,IN const RectF &)
title: RectF::Intersect(OUT RectF &,IN const RectF &,IN const RectF &) (gdiplustypes.h)
author: windows-sdk-content
description: The RectF::Intersect method determines the intersection of two rectangles and stores the result in a RectF object.
old-location: gdiplus\_gdiplus_CLASS_RectF_Intersect_c_a_b_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\rectfclass\rectfmethods\rectfintersectmethods\intersect_1c_a_b.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Intersect, Intersect method [GDI+], Intersect method [GDI+],RectF class, RectF class [GDI+],Intersect method, RectF.Intersect, RectF.Intersect(OUT RectF &,IN const RectF &,IN const RectF &), RectF.Intersect(RectF&,const RectF&,const RectF&), RectF::Intersect, RectF::Intersect(OUT RectF &,IN const RectF &,IN const RectF &), _gdiplus_CLASS_RectF_Intersect_c_a_b_, gdiplus._gdiplus_CLASS_RectF_Intersect_c_a_b_
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
 - RectF.Intersect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# RectF::Intersect(OUT RectF &,IN const RectF &,IN const RectF &)


## -description


The <b>RectF::Intersect</b> method determines the intersection of two rectangles and stores the result in a 
			<a href="https://msdn.microsoft.com/en-us/library/ms534497(v=VS.85).aspx">RectF</a> object.


## -parameters




### -param c [out]

Type: <b>RectF&amp;</b>

Reference to a 
					<a href="https://msdn.microsoft.com/en-us/library/ms534497(v=VS.85).aspx">RectF</a> object that receives the intersection of the two rectangles. 


### -param a [in]

Type: <b>const RectF&amp;</b>

Reference to one of the two rectangles to be intersected. 


### -param b [in]

Type: <b>const RectF&amp;</b>

Reference to one of the two rectangles to be intersected. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the intersection of the two rectangles is not empty, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534945(v=VS.85).aspx">Intersect Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536372(v=VS.85).aspx">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534497(v=VS.85).aspx">RectF</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533855(v=VS.85).aspx">Using a Pen to Draw Lines and Rectangles</a>
 

 

