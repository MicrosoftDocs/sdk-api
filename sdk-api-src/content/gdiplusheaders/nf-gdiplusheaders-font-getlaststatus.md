---
UID: NF:gdiplusheaders.Font.GetLastStatus
title: Font::GetLastStatus
author: windows-sdk-content
description: The Font::GetLastStatus method returns a value that indicates the nature of this Font object's most recent method failure.
old-location: gdiplus\_gdiplus_CLASS_Font_GetLastStatus_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontclass\fontmethods\getlaststatus_84.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Font class [GDI+],GetLastStatus method, Font.GetLastStatus, Font::GetLastStatus, GetLastStatus, GetLastStatus method [GDI+], GetLastStatus method [GDI+],Font class, _gdiplus_CLASS_Font_GetLastStatus_, gdiplus._gdiplus_CLASS_Font_GetLastStatus_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusheaders.h
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
 - Font.GetLastStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Font::GetLastStatus


## -description


The <b>Font::GetLastStatus</b> method returns a value that indicates the nature of this 
			<a href="https://msdn.microsoft.com/en-us/library/ms534437(v=VS.85).aspx">Font</a> object's most recent method failure.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

The <b>Font::GetLastStatus</b> method returns an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If no methods invoked on this 
						<a href="https://msdn.microsoft.com/en-us/library/ms534437(v=VS.85).aspx">Font</a> object have failed, then <b>Font::GetLastStatus</b> returns Ok.

If at least one method invoked on this 
						<a href="https://msdn.microsoft.com/en-us/library/ms534437(v=VS.85).aspx">Font</a> object has failed, then <b>Font::GetLastStatus</b> returns a value that indicates the nature of the most recent failure.




## -remarks



You can call <b>Font::GetLastStatus</b> immediately after constructing a 
				<a href="https://msdn.microsoft.com/en-us/library/ms534437(v=VS.85).aspx">Font</a> object to determine whether the constructor succeeded.

The first time you call the <b>Font::GetLastStatus</b> method of a 
				<a href="https://msdn.microsoft.com/en-us/library/ms534437(v=VS.85).aspx">Font</a> object, it returns Ok if the constructor succeeded and all methods invoked so far on the 
				<b>Font</b> object succeeded. Otherwise, it returns a value that indicates the nature of the most recent failure.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/en-us/library/ms534437(v=VS.85).aspx">Font</a> object, checks to see that the call to create the object was successful, and, if it was, uses the 
						<b>Font</b> object to draw text.


```cpp
VOID Example_GetLastStatus(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a Font object.
   Font myFont(L"Arial", 16);

   // Check the status of the last call.
   Status status = myFont.GetLastStatus();

   // If the call to create myFont succeeded, use myFont to write text.
   if (status == Ok)
   {
       SolidBrush solidbrush(Color(255, 0, 0, 0));
       WCHAR      string[] = L"The call succeeded";
       graphics.DrawString(string, 18, &myFont, PointF(0, 0), &solidbrush);
   }
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534437(v=VS.85).aspx">Font</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536200(v=VS.85).aspx">Font::IsAvailable</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533817(v=VS.85).aspx">Using Text and Fonts</a>
 

 

