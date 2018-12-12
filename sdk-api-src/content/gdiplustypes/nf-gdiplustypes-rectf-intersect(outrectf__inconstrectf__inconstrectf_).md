---
UID: NF:gdiplustypes.RectF.Intersect(OUT RectF &,IN const RectF &,IN const RectF &)
title: RectF::Intersect(OUT RectF &,IN const RectF &,IN const RectF &)
author: windows-sdk-content
description: The RectF::Intersect method determines the intersection of two rectangles and stores the result in a RectF object.
old-location: gdiplus\_gdiplus_CLASS_RectF_Intersect_c_a_b_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\rectfclass\rectfmethods\rectfintersectmethods\intersect_1c_a_b.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Intersect, Intersect method [GDI+], Intersect method [GDI+],RectF class, RectF class [GDI+],Intersect method, RectF.Intersect, RectF.Intersect(OUT RectF &,IN const RectF &,IN const RectF &), RectF.Intersect(RectF&,const RectF&,const RectF&), RectF::Intersect, RectF::Intersect(OUT RectF &,IN const RectF &,IN const RectF &), _gdiplus_CLASS_RectF_Intersect_c_a_b_, gdiplus._gdiplus_CLASS_RectF_Intersect_c_a_b_
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
			<a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a> object.


## -parameters




### -param c [out]

Type: <b>RectF&amp;</b>

Reference to a 
					<a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a> object that receives the intersection of the two rectangles. 


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




<a href="https://msdn.microsoft.com/4b57bc29-cec2-4a66-9227-6a31d8f1d4de">Intersect Methods</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>



<a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a>



<a href="https://msdn.microsoft.com/f2e4144f-f2f1-49db-bfdf-ffce3023b4cb">Using a Pen to Draw Lines and Rectangles</a>
 

 

