---
UID: NF:gdiplusheaders.Font.GetLastStatus
title: Font::GetLastStatus (gdiplusheaders.h)
description: The Font::GetLastStatus method returns a value that indicates the nature of this Font object's most recent method failure.
helpviewer_keywords: ["Font class [GDI+]","GetLastStatus method","Font.GetLastStatus","Font::GetLastStatus","GetLastStatus","GetLastStatus method [GDI+]","GetLastStatus method [GDI+]","Font class","_gdiplus_CLASS_Font_GetLastStatus_","gdiplus._gdiplus_CLASS_Font_GetLastStatus_"]
old-location: gdiplus\_gdiplus_CLASS_Font_GetLastStatus_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontclass\fontmethods\getlaststatus_84.htm
ms.date: 12/05/2018
ms.keywords: Font class [GDI+],GetLastStatus method, Font.GetLastStatus, Font::GetLastStatus, GetLastStatus, GetLastStatus method [GDI+], GetLastStatus method [GDI+],Font class, _gdiplus_CLASS_Font_GetLastStatus_, gdiplus._gdiplus_CLASS_Font_GetLastStatus_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Font::GetLastStatus
 - gdiplusheaders/Font::GetLastStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Font.GetLastStatus
---

# Font::GetLastStatus


## -description

The <b>Font::GetLastStatus</b> method returns a value that indicates the nature of this 
			<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a> object's most recent method failure.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

The <b>Font::GetLastStatus</b> method returns an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If no methods invoked on this 
						<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a> object have failed, then <b>Font::GetLastStatus</b> returns Ok.

If at least one method invoked on this 
						<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a> object has failed, then <b>Font::GetLastStatus</b> returns a value that indicates the nature of the most recent failure.

## -remarks

You can call <b>Font::GetLastStatus</b> immediately after constructing a 
				<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a> object to determine whether the constructor succeeded.

The first time you call the <b>Font::GetLastStatus</b> method of a 
				<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a> object, it returns Ok if the constructor succeeded and all methods invoked so far on the 
				<b>Font</b> object succeeded. Otherwise, it returns a value that indicates the nature of the most recent failure.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a> object, checks to see that the call to create the object was successful, and, if it was, uses the 
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

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-font-isavailable">Font::IsAvailable</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-text-and-fonts-use">Using Text and Fonts</a>
