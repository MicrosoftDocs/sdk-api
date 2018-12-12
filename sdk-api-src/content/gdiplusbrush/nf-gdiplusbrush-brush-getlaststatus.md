---
UID: NF:gdiplusbrush.Brush.GetLastStatus
title: Brush::GetLastStatus
author: windows-sdk-content
description: The Brush::GetLastStatus method returns a value that indicates the nature of this Brush object's most recent method failure.
old-location: gdiplus\_gdiplus_CLASS_Brush_GetLastStatus_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\brushclass\brushmethods\getlaststatus.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Brush class [GDI+],GetLastStatus method, Brush.GetLastStatus, Brush::GetLastStatus, GetLastStatus, GetLastStatus method [GDI+], GetLastStatus method [GDI+],Brush class, _gdiplus_CLASS_Brush_GetLastStatus_, gdiplus._gdiplus_CLASS_Brush_GetLastStatus_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusbrush.h
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
 - Brush.GetLastStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Brush::GetLastStatus


## -description


The <b>Brush::GetLastStatus</b> method returns a value that indicates the nature of this 
			<a href="https://msdn.microsoft.com/en-us/library/ms534424(v=VS.85).aspx">Brush</a> object's most recent method failure.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

The <b>Brush::GetLastStatus</b> method returns an element of the 	<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If no methods invoked on this 
						<a href="https://msdn.microsoft.com/en-us/library/ms534424(v=VS.85).aspx">Brush</a> object have failed since the previous call to <b>Brush::GetLastStatus</b>, then <b>Brush::GetLastStatus</b> returns Ok.

If at least one method invoked on this 
						<a href="https://msdn.microsoft.com/en-us/library/ms534424(v=VS.85).aspx">Brush</a> object has failed since the previous call to <b>Brush::GetLastStatus</b>, then <b>Brush::GetLastStatus</b> returns a value that indicates the nature of the most recent failure.




## -remarks



You can call <b>Brush::GetLastStatus</b> immediately after constructing a 
				<a href="https://msdn.microsoft.com/en-us/library/ms534424(v=VS.85).aspx">Brush</a> object to determine whether the constructor succeeded.

The first time you call the <b>Brush::GetLastStatus</b> method of a 
				<a href="https://msdn.microsoft.com/en-us/library/ms534424(v=VS.85).aspx">Brush</a> object, it returns Ok if the constructor succeeded and all methods invoked so far on the 
				<b>Brush</b> object succeeded. Otherwise, it returns a value that indicates the nature of the most recent failure.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/en-us/library/ms534508(v=VS.85).aspx">SolidBrush</a> object 
						<b>solidBrush</b> and checks the status of the call used to create 
						<b>solidBrush</b>. Then, if the call was successful, the code uses 
						<b>solidBrush</b> to fill a rectangle.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetLastStatus(HDC hdc)
{
   Graphics graphics(hdc);
   // Create a SolidBrush object.
   SolidBrush solidBrush(Color(255, 0, 255, 0));
   // Get the status of the last call.
   Status lastStatus = solidBrush.GetLastStatus();
   //If the call to create myBrush was successful, use it to fill a rectangle.
   if (lastStatus == Ok)
       graphics.FillRectangle(&amp;solidBrush, Rect(0, 0, 100, 100)); 
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534424(v=VS.85).aspx">Brush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534459(v=VS.85).aspx">HatchBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534473(v=VS.85).aspx">LinearGradientBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534508(v=VS.85).aspx">SolidBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534512(v=VS.85).aspx">TextureBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533811(v=VS.85).aspx">Using a Brush to Fill Shapes</a>
 

 

