---
UID: NF:gdipluspen.Pen.Pen(IN const Brush,IN REAL)
title: Pen::Pen(IN const Brush,IN REAL)
author: windows-sdk-content
description: Creates a Pen object that uses the attributes of a brush and a real number to set the width of this Pen object.
old-location: gdiplus\_gdiplus_CLASS_Pen_Pen_brush_width_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penconstructors\pen_34brush_width.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: Pen, Pen class [GDI+],Pen constructor, Pen constructor [GDI+], Pen constructor [GDI+],Pen class, Pen.Pen, Pen.Pen(IN const Brush,IN REAL), Pen.Pen(const Brush*,REAL), Pen::Pen, Pen::Pen(IN const Brush,IN REAL), _gdiplus_CLASS_Pen_Pen_brush_width_, gdiplus._gdiplus_CLASS_Pen_Pen_brush_width_
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
 - Pen.Pen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Pen::Pen(IN const Brush,IN REAL)


## -description


Creates a <a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> object that uses the attributes of a brush and a real number to set the width of this <b>Pen</b> object.


## -parameters




### -param brush [in]

Type: <b>const <a href="https://msdn.microsoft.com/37cfc0f8-8e17-4944-85fc-cc80ebff13df">Brush</a>*</b>

Pointer to a brush to base this pen on. 


### -param width [in]

Type: <b>REAL</b>

Optional. Real number that specifies the width of this pen's stroke. The default value is 1.0. 


## -remarks



If you pass the address of a pen to one of the draw methods of a 
				<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object, the width of the pen's stroke is dependent on the unit of measure specified in the 
				<b>Graphics</b> object. The default unit of measure is <b>UnitPixel</b>, which is an element of the 
				<a href="https://msdn.microsoft.com/33f0b0fd-7764-48bc-874e-26cc522d5362">Unit</a> enumeration.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/37cfc0f8-8e17-4944-85fc-cc80ebff13df">Brush</a> object and then creates a <a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> object based on the <b>Brush</b> object.


```cpp
SolidBrush sBrush(Color(255,255,0,0));
Pen pen(&sBrush, 4.0f);
```





## -see-also




<a href="https://msdn.microsoft.com/37cfc0f8-8e17-4944-85fc-cc80ebff13df">Brush</a>



<a href="https://msdn.microsoft.com/30b58e23-b79a-4746-8b2a-d19711ddcd69">Pen</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/b529ba0b-1786-4925-88bd-1a8369fc368c">Setting Pen Width and Alignment</a>
 

 

