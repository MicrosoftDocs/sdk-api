---
UID: NF:gdipluspen.Pen.GetDashPattern
title: Pen::GetDashPattern
author: windows-sdk-content
description: The Pen::GetDashPattern method gets an array of custom dashes and spaces currently set for this Pen object.
old-location: gdiplus\_gdiplus_CLASS_Pen_GetDashPattern_dashArray_count_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\getdashpattern.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetDashPattern, GetDashPattern method [GDI+], GetDashPattern method [GDI+],Pen class, Pen class [GDI+],GetDashPattern method, Pen.GetDashPattern, Pen::GetDashPattern, _gdiplus_CLASS_Pen_GetDashPattern_dashArray_count_, gdiplus._gdiplus_CLASS_Pen_GetDashPattern_dashArray_count_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdipluspen.h
req.include-header: Gdiplus.h
req.redist: 
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
 - Pen.GetDashPattern
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Pen::GetDashPattern


## -description


The <b>Pen::GetDashPattern</b> method gets an array of custom dashes and spaces currently set for this 
			<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> object.


## -parameters




### -param dashArray [out]

Type: <b>REAL*</b>

Pointer to an array that receives the length of the dashes and spaces in a custom dashed line. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the 
<i>dashArray</i> array. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



The elements in the 
				<i>dashArray</i> array set the length of each dash and space in the dash pattern. The first element sets the length of a dash, the second element sets the length of a space, the third element sets the length of a dash, and so forth.

The length of each dash and space in the dash pattern is the product of each element in the array and the width of the 
				<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> object.


#### Examples



The following example creates an array of real numbers and a 
						<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> object, sets the dash pattern, and draws a custom dashed line. The code then gets the dash pattern currently set for the pen.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetDashPattern(HDC hdc
{
   Graphics graphics(hdc);

   // Create a custom dashed pen, and use it to draw a line.
   REAL dashVals[4] = {5, 2, 15, 4};
   Pen pen(Color(255, 0, 0, 0), 5);
   pen.SetDashPattern(dashVals, 4);
   graphics.DrawLine(&amp;pen, 5, 20, 405, 200);

   // Obtain information about the pen.
   INT count = 0;
   REAL* dashValues = NULL;

   count = pen.GetDashPatternCount();
   dashValues = new REAL[count];
   pen.GetDashPattern(dashValues, count);

   for(INT j = 0; j &lt; count; ++j)
   {
      // Inspect or use the value in dashValues[j].
   }
   delete [] dashValues;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533850(v=VS.85).aspx">Drawing a Custom Dashed Line</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535027(v=VS.85).aspx">Pen::GetDashPatternCount</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535049(v=VS.85).aspx">Pen::SetDashPattern</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536372(v=VS.85).aspx">Pens, Lines, and Rectangles</a>
 

 

