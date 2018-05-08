---
UID: NF:gdipluspen.Pen.SetColor
title: Pen::SetColor
author: windows-driver-content
description: The Pen::SetColor method sets the color for this Pen object.
old-location: gdiplus\_gdiplus_CLASS_Pen_SetColor_color_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setcolor.htm
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: Pen class [GDI+],SetColor method, Pen.SetColor, Pen::SetColor, SetColor, SetColor method [GDI+], SetColor method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetColor_color_, gdiplus._gdiplus_CLASS_Pen_SetColor_color_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdipluspen.h
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
req.typenames: WmfPlaceableFileHeader
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	Pen.SetColor
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Pen::SetColor


## -description


The <b>Pen::SetColor</b> method sets the color for this 
			<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object.


## -parameters




### -param color [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a></b>

Reference to a <a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a> object that specifies the color for this 
					<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/4121c28f-0402-46fa-9501-0e41de21bae5">Pen::GetColor</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/f2e4144f-f2f1-49db-bfdf-ffce3023b4cb">Using a Pen to Draw Lines and Rectangles</a>
 

 

