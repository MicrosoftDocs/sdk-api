---
UID: NF:gdiplusheaders.FontFamily.GetLastStatus
title: FontFamily::GetLastStatus (gdiplusheaders.h)
description: The FontFamily::GetLastStatus method returns a value that indicates the nature of this FontFamily object's most recent method failure.
helpviewer_keywords: ["FontFamily class [GDI+]","GetLastStatus method","FontFamily.GetLastStatus","FontFamily::GetLastStatus","GetLastStatus","GetLastStatus method [GDI+]","GetLastStatus method [GDI+]","FontFamily class","_gdiplus_CLASS_FontFamily_GetLastStatus_","gdiplus._gdiplus_CLASS_FontFamily_GetLastStatus_"]
old-location: gdiplus\_gdiplus_CLASS_FontFamily_GetLastStatus_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontfamilyclass\fontfamilymethods\getlaststatus_12.htm
ms.date: 12/05/2018
ms.keywords: FontFamily class [GDI+],GetLastStatus method, FontFamily.GetLastStatus, FontFamily::GetLastStatus, GetLastStatus, GetLastStatus method [GDI+], GetLastStatus method [GDI+],FontFamily class, _gdiplus_CLASS_FontFamily_GetLastStatus_, gdiplus._gdiplus_CLASS_FontFamily_GetLastStatus_
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
 - FontFamily::GetLastStatus
 - gdiplusheaders/FontFamily::GetLastStatus
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
 - FontFamily.GetLastStatus
---

# FontFamily::GetLastStatus


## -description

The <b>FontFamily::GetLastStatus</b> method returns a value that indicates the nature of this <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily">FontFamily</a> object's most recent method failure.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

The <b>FontFamily::GetLastStatus</b> method returns an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If no methods invoked on this <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily">FontFamily</a> object have failed since the previous call to <b>FontFamily::GetLastStatus</b>, then <b>FontFamily::GetLastStatus</b> returns Ok.

If at least one method invoked on this <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily">FontFamily</a> object has failed since the previous call to <b>FontFamily::GetLastStatus</b>, then <b>FontFamily::GetLastStatus</b> returns a value that indicates the nature of the most recent failure.

## -remarks

You can call <b>FontFamily::GetLastStatus</b> immediately after constructing a <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily">FontFamily</a> object to determine whether the constructor succeeded.

The first time you call the <b>FontFamily::GetLastStatus</b> method of a 
<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily">FontFamily</a> object, it returns Ok if the constructor succeeded and all methods invoked so far on the <b>FontFamily</b> object succeeded. Otherwise, it returns a value that indicates the nature of the most recent failure.


#### Examples



The following example creates a <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily">FontFamily</a> object and then checks the status of the call to create the object. If the call was successful, the example draws text.


```cpp
VOID Example_GetLastStatus(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a FontFamily object.
   FontFamily myFontFamily(L"arial");
   
   // Check the status of the last call.
   Status status = myFontFamily.GetLastStatus();

   // If the last call succeeded, draw text.
   if (status ==Ok)
   {
       SolidBrush solidbrush(Color(255, 0, 0, 0));
       Font       font(&myFontFamily, 16);
       WCHAR      string[] = L"status = Ok";
       graphics.DrawString(string, -1, &font, PointF(0, 0), &solidbrush);
   }
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-constructing-font-families-and-fonts-use">Constructing Font Families and Fonts</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily">FontFamily</a>



<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>
