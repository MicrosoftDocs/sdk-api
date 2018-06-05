---
UID: NF:gdiplusstringformat.StringFormat.GenericTypographic
title: StringFormat::GenericTypographic
author: windows-sdk-content
description: The StringFormat::GenericTypographic method creates a generic, typographic StringFormat object.
old-location: gdiplus\_gdiplus_CLASS_StringFormat_GenericTypographic_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\stringformatclass\stringformatmethods\generictypographic.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GenericTypographic, GenericTypographic method [GDI+], GenericTypographic method [GDI+],StringFormat class, StringFormat class [GDI+],GenericTypographic method, StringFormat.GenericTypographic, StringFormat::GenericTypographic, _gdiplus_CLASS_StringFormat_GenericTypographic_, gdiplus._gdiplus_CLASS_StringFormat_GenericTypographic_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusstringformat.h
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	StringFormat.GenericTypographic
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# StringFormat::GenericTypographic


## -description


The <b>StringFormat::GenericTypographic</b> method creates a generic, typographic 
			<a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a> object.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a>*</b>
</strong>

This method returns a pointer to the new 
						<a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a> object.




## -remarks



A generic, typographic 
				<a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a> object has the following characteristics: 

<ul>
<li>String format flags StringFormatFlagsLineLimit, StringFormatFlagsNoClip, and StringFormatFlagsNoFitBlackBox are set. </li>
<li>Character alignment and line alignment are set to StringAlignmentNear. </li>
<li>Language ID is set to neutral language, which means that the current language associated with the calling thread is used. </li>
<li>String digit substitution is set to StringDigitSubstituteUser. </li>
<li>Hot key prefix is set to HotkeyPrefixNone. </li>
<li>Number of tab stops is set to zero. </li>
<li>String trimming is set to StringTrimmingNone. </li>
</ul>

#### Examples



The following example creates a generic, typographic 
						<a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a> object and then uses it to draw a formatted string. The code also draws the string's layout rectangle.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GenericTypographic(HDC hdc)
{
   Graphics graphics(hdc);
   SolidBrush  solidBrush(Color(255, 255, 0, 0)); 
   FontFamily  fontFamily(L"Times New Roman");
   Font        font(&amp;fontFamily, 12, FontStyleRegular, UnitPoint);
   
   // Create a generic typographic StringFormat object.
   const StringFormat* pStringFormat = StringFormat::GenericTypographic();
   // Use the generic typographic StringFormat object 
   // in a call to DrawString.
  graphics.DrawString(
      L"Formatted by a generic typographic StringFormat object", 
      54,  // string length
      &amp;font, 
      RectF(30, 30, 100, 120), 
      pStringFormat, 
      &amp;solidBrush);
   // Draw the rectangle that encloses the text.
   Pen pen(Color(255, 255, 0, 0));
   graphics.DrawRectangle(&amp;pen, 30, 30, 100, 120);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/dd8af524-688c-44dd-b3e4-deadb874bdc3">Font</a>



<a href="https://msdn.microsoft.com/79b7fa3b-55f8-4ac8-814d-82e4f8280863">HotkeyPrefix</a>



<a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a>



<a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a>



<a href="https://msdn.microsoft.com/d395f6b4-8d8a-41b1-9c49-6fc2f005ca5d">StringAlignment</a>



<a href="https://msdn.microsoft.com/b61e9a88-2b00-43f5-bc8d-1d6b4d6ecb19">StringDigitSubstitute</a>



<a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a>



<a href="https://msdn.microsoft.com/9bbddab0-46b1-49db-86c1-cf9086692958">StringFormatFlags</a>



<a href="https://msdn.microsoft.com/8ecaabac-dfc6-47ca-91e3-9f577be77b5f">StringTrimming</a>
 

 

