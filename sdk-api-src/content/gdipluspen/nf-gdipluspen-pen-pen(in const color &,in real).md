---
UID: NF:gdipluspen.Pen.Pen(IN const Color &,IN REAL)
title: Pen::Pen(IN const Color &,IN REAL)
author: windows-sdk-content
description: Creates a Pen object that uses a specified color and width.
old-location: gdiplus\_gdiplus_CLASS_Pen_Pen_color_width_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penconstructors\pen_36color_width.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: Pen, Pen class [GDI+],Pen constructor, Pen constructor [GDI+], Pen constructor [GDI+],Pen class, Pen.Pen, Pen.Pen(IN const Color &,IN REAL), Pen.Pen(const Color&,REAL), Pen::Pen, Pen::Pen(IN const Color &,IN REAL), _gdiplus_CLASS_Pen_Pen_color_width_, gdiplus._gdiplus_CLASS_Pen_Pen_color_width_
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
- apiref
: 
- COM
: 
- gdipluspen.h
: 
- Pen.Pen
: 
req.product: GDI+ 1.0
---

# Pen::Pen(IN const Color &,IN REAL)


## -description


Creates a <a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object that uses a specified color and width.


## -parameters




### -param color [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a></b>

Reference to a <a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a> object that specifies the color for this <a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object. 


### -param width [in]

Type: <b>REAL</b>

Optional. Real number that specifies the width of this pen's stroke. The default value is 1.0. 


## -remarks



If you pass the address of a pen to one of the draw methods of a 
				<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object, the width of the pen's stroke is dependent on the unit of measure specified in the 
				<b>Graphics</b> object. The default unit of measure is <b>UnitPixel</b>, which is an element of the 
				<a href="https://msdn.microsoft.com/33f0b0fd-7764-48bc-874e-26cc522d5362">Unit</a> enumeration.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object with the color red and a width of 4.0.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>Pen pen(Color(255,255,0,0), 4.0f); </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>



<a href="https://msdn.microsoft.com/30b58e23-b79a-4746-8b2a-d19711ddcd69">Pen</a>



<a href="https://msdn.microsoft.com/f86b8bdd-127c-4dc4-88c2-8a1b6fec19bf">Pen::SetWidth</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/b529ba0b-1786-4925-88bd-1a8369fc368c">Setting Pen Width and Alignment</a>
 

 

