---
UID: NF:gdiplustypes.SizeF.Empty
title: SizeF::Empty
author: windows-sdk-content
description: The SizeF::Empty method determines whether a SizeF object is empty.
old-location: gdiplus\_gdiplus_CLASS_SizeF_Empty_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\sizefclass\sizefmethods\empty_16.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Empty, Empty method [GDI+], Empty method [GDI+],SizeF class, SizeF class [GDI+],Empty method, SizeF.Empty, SizeF::Empty, _gdiplus_CLASS_SizeF_Empty_, gdiplus._gdiplus_CLASS_SizeF_Empty_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplustypes.h
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - SizeF.Empty
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# SizeF::Empty


## -description


The <b>SizeF::Empty</b> method determines whether a 
			<a href="https://msdn.microsoft.com/en-us/library/ms534506(v=VS.85).aspx">SizeF</a> object is empty.


## -parameters






## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the 
						<b>Width</b> and 
						<b>Height</b> data members are both equal to zero, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -remarks



A 
				<a href="https://msdn.microsoft.com/en-us/library/ms534506(v=VS.85).aspx">SizeF</a> object is defined as empty if the 
				<b>Width</b> and 
				<b>Height</b> data members are both equal to zero.


#### Examples



<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>RectF rect(50.0f, 50.0f, 100.0f, 200.0f);
SizeF size;

rect.Inflate(-50.0f, -100.0f);
rect.GetSize(&amp;size);

if(size.Empty())
{

   // The width and height are both 0.
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534497(v=VS.85).aspx">RectF</a>



<a href="https://msdn.microsoft.com/d5be390d-11c7-47e3-8cd0-335fb6b031fd">Size</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534506(v=VS.85).aspx">SizeF</a>
 

 

