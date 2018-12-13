---
UID: NF:gdiplustypes.Size.operator-add
title: Size::operator-add
author: windows-sdk-content
description: The Size::operator+ method adds the Width and Height data members of two Size objects.
old-location: gdiplus\_gdiplus_CLASS_Size_operator_opadd_sz_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\sizeclass\sizemethods\operatorplus_84sz.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Size class [GDI+],operator+ method, Size.operator+, Size.operator+(const Size&), Size.operator-add, Size::operator+, Size::operator-add, _gdiplus_CLASS_Size_operator_opadd_sz_, gdiplus._gdiplus_CLASS_Size_operator_opadd_sz_, operator+, operator+ method [GDI+], operator+ method [GDI+],Size class
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
 - Size.operator+
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Size::operator-add


## -description


The <b>Size::operator+</b> method adds the <b>Width</b> and <b>Height</b> data members of two <a href="https://msdn.microsoft.com/d5be390d-11c7-47e3-8cd0-335fb6b031fd">Size</a> objects.


## -parameters




### -param sz [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/d5be390d-11c7-47e3-8cd0-335fb6b031fd">Size</a></b>

Reference to a <a href="https://msdn.microsoft.com/d5be390d-11c7-47e3-8cd0-335fb6b031fd">Size</a> object whose <b>Width</b> and <b>Height</b> data members are added to the <b>Width</b> and <b>Height</b> data members of this <b>Size</b> object. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/d5be390d-11c7-47e3-8cd0-335fb6b031fd">Size</a></b>
</strong>

This method returns the sum of this <a href="https://msdn.microsoft.com/d5be390d-11c7-47e3-8cd0-335fb6b031fd">Size</a> object and another <b>Size</b> object.




## -remarks



This method overloads the addition operator for <a href="https://msdn.microsoft.com/d5be390d-11c7-47e3-8cd0-335fb6b031fd">Size</a> objects. If A, B, and C are <b>Size</b> objects, the statement <b>C = A + B</b> is equivalent to <b>C = A.operator+(B)</b>.


#### Examples



<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_OperatorPlus(HDC hdc)
{
   Graphics graphics(hdc);
   Pen pen(Color(255, 0, 0, 0));

   Size size1(80, 30);
   Size size2(50, 20);
   
   Size size3 = size1 + size2;

   graphics.DrawRectangle(&amp;pen, 50, 50, size1.Width, size1.Height);
   graphics.DrawRectangle(&amp;pen, 50, 50, size2.Width, size2.Height);
   graphics.DrawRectangle(&amp;pen, 50, 50, size3.Width, size3.Height);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d5be390d-11c7-47e3-8cd0-335fb6b031fd">Size</a>



<a href="https://msdn.microsoft.com/48711dd6-74eb-41fd-9a07-0be4ad7582a4">Size::operator-</a>



<a href="https://msdn.microsoft.com/b40ade07-f89e-44ba-9185-9aec01f1051f">SizeF</a>
 

 

