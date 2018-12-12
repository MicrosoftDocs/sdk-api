---
UID: NF:gdiplustypes.Size.operator-sub
title: Size::operator-sub
author: windows-sdk-content
description: The Size::operator- method subtracts the Width and Height data members of two Size objects.
old-location: gdiplus\_gdiplus_CLASS_Size_operator_opminus_sz_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\sizeclass\sizemethods\operator_81sz.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Size class [GDI+],operator- method, Size.operator-, Size.operator-(const Size&), Size.operator-sub, Size::operator-, Size::operator-sub, _gdiplus_CLASS_Size_operator_opminus_sz_, gdiplus._gdiplus_CLASS_Size_operator_opminus_sz_, operator-, operator- method [GDI+], operator- method [GDI+],Size class
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
 - Size.operator-
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Size::operator-sub


## -description


The <b>Size::operator-</b> method subtracts the <b>Width</b> and <b>Height</b> data members of two <a href="https://msdn.microsoft.com/d5be390d-11c7-47e3-8cd0-335fb6b031fd">Size</a> objects.


## -parameters




### -param sz [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/d5be390d-11c7-47e3-8cd0-335fb6b031fd">Size</a></b>

Reference to a <a href="https://msdn.microsoft.com/d5be390d-11c7-47e3-8cd0-335fb6b031fd">Size</a> object whose <b>Width</b> and <b>Height</b> data members are subtracted from the <b>Width</b> and <b>Height</b> data members of this <b>Size</b> object. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/d5be390d-11c7-47e3-8cd0-335fb6b031fd">Size</a></b>
</strong>

This method returns the difference of this <a href="https://msdn.microsoft.com/d5be390d-11c7-47e3-8cd0-335fb6b031fd">Size</a> object and another <b>Size</b> object.




## -remarks



This method overloads the subtraction operator for <a href="https://msdn.microsoft.com/d5be390d-11c7-47e3-8cd0-335fb6b031fd">Size</a> objects. If A, B, and C are <b>Size</b> objects, the statement <b>C = A - B</b> is equivalent to <b>C = A.operator-(B)</b>.


#### Examples



<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_OperatorMinus(HWND hWnd)
{
   Graphics graphics(hdc);
   Pen pen(Color(255, 0, 0, 0));

   Size size1(200, 100);
   Size size2(50, 40);
   
   Size size3 = size1 - size2;

   graphics.DrawRectangle(&amp;pen, 50, 50, size1.Width, size1.Height);
   graphics.DrawRectangle(&amp;pen, 50, 50, size2.Width, size2.Height);
   graphics.DrawRectangle(&amp;pen, 50, 50, size3.Width, size3.Height);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d5be390d-11c7-47e3-8cd0-335fb6b031fd">Size</a>



<a href="https://msdn.microsoft.com/4fd88c51-dcf1-4682-9bae-8821c5d553eb">Size::operator+</a>



<a href="https://msdn.microsoft.com/b40ade07-f89e-44ba-9185-9aec01f1051f">SizeF</a>
 

 

