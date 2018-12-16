---
UID: NF:gdiplustypes.SizeF.Equals
title: SizeF::Equals
author: windows-sdk-content
description: The SizeF::Equals method determines whether two SizeF objects are equal.
old-location: gdiplus\_gdiplus_CLASS_SizeF_Equals_sz_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\sizefclass\sizefmethods\equals_12sz.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Equals, Equals method [GDI+], Equals method [GDI+],SizeF class, SizeF class [GDI+],Equals method, SizeF.Equals, SizeF::Equals, _gdiplus_CLASS_SizeF_Equals_sz_, gdiplus._gdiplus_CLASS_SizeF_Equals_sz_
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
 - SizeF.Equals
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# SizeF::Equals


## -description


The <b>SizeF::Equals</b> method determines whether two 
			<a href="https://msdn.microsoft.com/en-us/library/ms534506(v=VS.85).aspx">SizeF</a> objects are equal.


## -parameters




### -param sz [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534506(v=VS.85).aspx">SizeF</a></b>

Reference to a 
					<a href="https://msdn.microsoft.com/en-us/library/ms534506(v=VS.85).aspx">SizeF</a> object that is compared to this 
					<b>SizeF</b> object. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the 
						<b>Width</b> and 
						<b>Height</b> data members of the two 
						<a href="https://msdn.microsoft.com/en-us/library/ms534506(v=VS.85).aspx">SizeF</a> objects are equal, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -remarks



Two 
				<a href="https://msdn.microsoft.com/en-us/library/ms534506(v=VS.85).aspx">SizeF</a> objects are defined as equal if the 
				<b>Width</b> and 
				<b>Height</b> data members are equal.


#### Examples



<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>RectF rect(50.0f, 30.0f, 200.0f, 100.0f);
SizeF desiredSizeF(200.0f, 100.0f);
SizeF rectSizeF;

// Get the size of the rectangle.
rect.GetSize(&amp;rectSizeF);

if(rectSizeF.Equals(desiredSizeF))
{
   // The rectangle has the wanted size.
} </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534497(v=VS.85).aspx">RectF</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534747(v=VS.85).aspx">Size Constructors</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534506(v=VS.85).aspx">SizeF</a>
 

 

