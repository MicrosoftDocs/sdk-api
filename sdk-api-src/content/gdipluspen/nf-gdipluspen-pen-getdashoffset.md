---
UID: NF:gdipluspen.Pen.GetDashOffset
title: Pen::GetDashOffset
author: windows-sdk-content
description: The Pen::GetDashOffset method gets the distance from the start of the line to the start of the first space in a dashed line.
old-location: gdiplus\_gdiplus_CLASS_Pen_GetDashOffset_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\getdashoffset.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetDashOffset, GetDashOffset method [GDI+], GetDashOffset method [GDI+],Pen class, Pen class [GDI+],GetDashOffset method, Pen.GetDashOffset, Pen::GetDashOffset, _gdiplus_CLASS_Pen_GetDashOffset_, gdiplus._gdiplus_CLASS_Pen_GetDashOffset_
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WmfPlaceableFileHeader
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>REAL dashOffset = dashPen.GetDashOffset();</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/ms533850(v=VS.85).aspx">Drawing a Custom Dashed Line</a>



<a href="https://msdn.microsoft.com/library/ms534485(v=VS.85).aspx">Pen</a>



<a href="https://msdn.microsoft.com/library/ms535048(v=VS.85).aspx">Pen::SetDashOffset</a>



<a href="https://msdn.microsoft.com/library/ms536372(v=VS.85).aspx">Pens, Lines, and Rectangles</a>
 

 

