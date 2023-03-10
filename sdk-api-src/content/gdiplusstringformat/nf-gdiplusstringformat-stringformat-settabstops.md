---
UID: NF:gdiplusstringformat.StringFormat.SetTabStops
title: StringFormat::SetTabStops (gdiplusstringformat.h)
description: The StringFormat::SetTabStops method sets the offsets for tab stops in this StringFormat object.
helpviewer_keywords: ["SetTabStops","SetTabStops method [GDI+]","SetTabStops method [GDI+]","StringFormat class","StringFormat class [GDI+]","SetTabStops method","StringFormat.SetTabStops","StringFormat::SetTabStops","_gdiplus_CLASS_StringFormat_SetTabStops_firstTabOffset_count_tabStops_","gdiplus._gdiplus_CLASS_StringFormat_SetTabStops_firstTabOffset_count_tabStops_"]
old-location: gdiplus\_gdiplus_CLASS_StringFormat_SetTabStops_firstTabOffset_count_tabStops_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\stringformatclass\stringformatmethods\settabstops.htm
ms.date: 12/05/2018
ms.keywords: SetTabStops, SetTabStops method [GDI+], SetTabStops method [GDI+],StringFormat class, StringFormat class [GDI+],SetTabStops method, StringFormat.SetTabStops, StringFormat::SetTabStops, _gdiplus_CLASS_StringFormat_SetTabStops_firstTabOffset_count_tabStops_, gdiplus._gdiplus_CLASS_StringFormat_SetTabStops_firstTabOffset_count_tabStops_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - StringFormat::SetTabStops
 - gdiplusstringformat/StringFormat::SetTabStops
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
 - StringFormat.SetTabStops
---

# StringFormat::SetTabStops


## -description

The <b>StringFormat::SetTabStops</b> method sets the offsets for tab stops in this 
			<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object.

## -parameters

### -param firstTabOffset [in]

Type: <b>REAL</b>

Real number that specifies the initial offset position. This initial offset position is relative to the string's origin and the offset of the first tab stop is relative to the initial offset position.

### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of tab-stop offsets in the 
					<i>tabStops</i> array.

### -param tabStops [in]

Type: <b>const REAL*</b>

Pointer to an array of real numbers that specify the tab-stop offsets. The offset of the first tab stop is the first value in the array, the offset of the second tab stop, the second value in the array, and so on.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

Each tab-stop offset in the 
				<i>tabStops</i> array, except the first one, is relative to the previous one. The first tab-stop offset is relative to the initial offset position specified by 
				<i>firstTabOffset</i>. For example, if the initial offset position is 8 and the first tab-stop offset is 50, then the first tab stop is at position 58. If the initial offset position is zero, then the first tab-stop offset is relative to position 0, the string origin.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object, sets tab stops, and uses the 
						<b>StringFormat</b> object to draw a string that contains tab characters (\t). The code also draws the string's layout rectangle.


```cpp
VOID Example_SetTabStops(HDC hdc)
{
   Graphics graphics(hdc);

   REAL         tabs[] = {150, 100, 100};
   FontFamily   fontFamily(L"Courier New");
   Font         font(&fontFamily, 12, FontStyleRegular, UnitPoint);
   SolidBrush   solidBrush(Color(255, 0, 0, 255));

   StringFormat stringFormat;
   stringFormat.SetTabStops(0, 3, tabs);
   graphics.DrawString(
      L"Name\tTest 1\tTest 2\tTest 3", 
      25, 
      &font, 
      RectF(20, 20, 500, 100), 
      &stringFormat, 
      &solidBrush);

   // Draw the rectangle that encloses the text.
   Pen pen(Color(255, 255, 0, 0));
   graphics.DrawRectangle(&pen, 20, 20, 500, 100);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-formatting-text-use">Formatting Text</a>



<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a>



<a href="/windows/desktop/api/gdiplusstringformat/nf-gdiplusstringformat-stringformat-gettabstops">StringFormat::GetTabStops</a>