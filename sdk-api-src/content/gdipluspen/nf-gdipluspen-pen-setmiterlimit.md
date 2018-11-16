---
UID: NF:gdipluspen.Pen.SetMiterLimit
title: Pen::SetMiterLimit
author: windows-sdk-content
description: The Pen::SetMiterLimit method sets the miter limit of this Pen object.
old-location: gdiplus\_gdiplus_CLASS_Pen_SetMiterLimit_miterLimit_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setmiterlimit.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Pen class [GDI+],SetMiterLimit method, Pen.SetMiterLimit, Pen::SetMiterLimit, SetMiterLimit, SetMiterLimit method [GDI+], SetMiterLimit method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetMiterLimit_miterLimit_, gdiplus._gdiplus_CLASS_Pen_SetMiterLimit_miterLimit_
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
 - Pen.SetMiterLimit
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
- Pen.SetMiterLimit
: 
req.product: GDI+ 1.0
---

# Pen::SetMiterLimit


## -description


The <b>Pen::SetMiterLimit</b> method sets the miter limit of this 
			<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object.


## -parameters




### -param miterLimit [in]

Type: <b>REAL</b>

Real number that specifies the miter limit of this 
					<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object. A real number value that is less than 1.0f will be replaced with 1.0f. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



The miter length is the distance from the intersection of the line walls on the inside of the join to the intersection of the line walls outside of the join. The miter length can be large when the angle between two lines is small. The miter limit is the maximum allowed ratio of miter length to stroke width. The default value is 10.0f.

If the miter length of the join of the intersection exceeds the limit of the join, then the join will be beveled to keep it within the limit of the join of the intersection.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object and sets the miter limit for the pen.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>Pen pen(Color(255,255,0,0), 4.0f);
Status stat = pen.SetMiterLimit(10.0f);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/4ec3e76a-2531-4869-a5b0-c595198e8345">Joining Lines</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/c6d35302-ff27-465d-9dc3-3e558ee7d672">Pen::GetMiterLimit</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>
 

 

