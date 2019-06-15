---
UID: NF:gdipluspen.Pen.GetDashOffset
title: Pen::GetDashOffset (gdipluspen.h)
author: windows-sdk-content
description: The Pen::GetDashOffset method gets the distance from the start of the line to the start of the first space in a dashed line.
old-location: gdiplus\_gdiplus_CLASS_Pen_GetDashOffset_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\getdashoffset.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDashOffset, GetDashOffset method [GDI+], GetDashOffset method [GDI+],Pen class, Pen class [GDI+],GetDashOffset method, Pen.GetDashOffset, Pen::GetDashOffset, _gdiplus_CLASS_Pen_GetDashOffset_, gdiplus._gdiplus_CLASS_Pen_GetDashOffset_
ms.topic: method
f1_keywords: ["gdipluspen/Pen.GetDashOffset"]
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
 - Pen.GetDashOffset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Pen::GetDashOffset


## -description


The <b>Pen::GetDashOffset</b> method gets the distance from the start of the line to the start of the first space in a dashed line.


## -parameters






## -returns



Type: <strong>Type: <b>REAL</b>
</strong>

This method returns a real number that indicates the distance from the start of the line to the start of the dashes.




## -remarks



A positive return value shifts the first dash forward along the path, and a negative return value shifts the start of the path forward along the first dash. 


#### Examples



The following example assumes that 
						<i>dashPen</i> has been defined with a certain dash style and gets the dash offset value.


```cpp
REAL dashOffset = dashPen.GetDashOffset();
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-drawing-a-custom-dashed-line-use">Drawing a Custom Dashed Line</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setdashoffset">Pen::SetDashOffset</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>
 

 

