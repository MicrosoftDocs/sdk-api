---
UID: NF:gdiplusstringformat.StringFormat.GenericDefault
title: StringFormat::GenericDefault
author: windows-sdk-content
description: The StringFormat::GenericDefault method creates a generic, default StringFormat object.
old-location: gdiplus\_gdiplus_CLASS_StringFormat_GenericDefault_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\stringformatclass\stringformatmethods\genericdefault.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GenericDefault, GenericDefault method [GDI+], GenericDefault method [GDI+],StringFormat class, StringFormat class [GDI+],GenericDefault method, StringFormat.GenericDefault, StringFormat::GenericDefault, _gdiplus_CLASS_StringFormat_GenericDefault_, gdiplus._gdiplus_CLASS_StringFormat_GenericDefault_
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - StringFormat.GenericDefault
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# StringFormat::GenericDefault


## -description


The <b>StringFormat::GenericDefault</b> method creates a generic, default 
			<a href="https://msdn.microsoft.com/en-us/library/ms534510(v=VS.85).aspx">StringFormat</a> object.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534510(v=VS.85).aspx">StringFormat</a>*</b>
</strong>

This method returns a pointer to the new 
						<a href="https://msdn.microsoft.com/en-us/library/ms534510(v=VS.85).aspx">StringFormat</a> object.




## -remarks



A generic, default 
				<a href="https://msdn.microsoft.com/en-us/library/ms534510(v=VS.85).aspx">StringFormat</a> object has the following characteristics: 

<ul>
<li>No string format flags are set. </li>
<li>Character alignment and line alignment are set to StringAlignmentNear. </li>
<li>Language ID is set to neutral language, which means that the current language associated with the calling thread is used. </li>
<li>String digit substitution is set to StringDigitSubstituteUser. </li>
<li>Hot key prefix is set to HotkeyPrefixNone. </li>
<li>Number of tab stops is set to zero. </li>
<li>String trimming is set to StringTrimmingCharacter. </li>
</ul>

#### Examples



The following example creates a generic, default 
						<a href="https://msdn.microsoft.com/en-us/library/ms534510(v=VS.85).aspx">StringFormat</a> object and then uses it to draw a formatted string. The code also draws the string's layout rectangle.


```cpp
VOID Example_GenericDefault(HDC hdc)
{
   Graphics graphics(hdc);

   SolidBrush  solidBrush(Color(255, 255, 0, 0)); 
   FontFamily  fontFamily(L"Times New Roman");
   Font        font(&fontFamily, 12, FontStyleRegular, UnitPoint);
   
   // Create a generic StringFormat object.
   const StringFormat* pStringFormat = StringFormat::GenericDefault();

   // Use the generic StringFormat object in a call to DrawString.
  graphics.DrawString(
      L"This text was formatted by a generic StringFormat object.", 
      57,  // string length
      &font, 
      RectF(30, 30, 100, 120), 
      pStringFormat, 
      &solidBrush);

   // Draw the rectangle that encloses the text.
   Pen pen(Color(255, 255, 0, 0));
   graphics.DrawRectangle(&pen, 30, 30, 100, 120);
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534437(v=VS.85).aspx">Font</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534131(v=VS.85).aspx">HotkeyPrefix</a>



<a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534497(v=VS.85).aspx">RectF</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534177(v=VS.85).aspx">StringAlignment</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534179(v=VS.85).aspx">StringDigitSubstitute</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534510(v=VS.85).aspx">StringFormat</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534181(v=VS.85).aspx">StringFormatFlags</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534403(v=VS.85).aspx">StringTrimming</a>
 

 

