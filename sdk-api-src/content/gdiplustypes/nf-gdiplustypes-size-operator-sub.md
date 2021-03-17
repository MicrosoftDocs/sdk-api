---
UID: NF:gdiplustypes.Size.operator-sub
title: Size::operator-sub (gdiplustypes.h)
description: The Size::operator- method subtracts the Width and Height data members of two Size objects.
helpviewer_keywords: ["Size class [GDI+]","operator- method","Size.operator-","Size.operator-(const Size&)","Size.operator-sub","Size::operator-","Size::operator-sub","_gdiplus_CLASS_Size_operator_opminus_sz_","gdiplus._gdiplus_CLASS_Size_operator_opminus_sz_","operator-","operator- method [GDI+]","operator- method [GDI+]","Size class"]
old-location: gdiplus\_gdiplus_CLASS_Size_operator_opminus_sz_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\sizeclass\sizemethods\operator_81sz.htm
ms.date: 12/05/2018
ms.keywords: Size class [GDI+],operator- method, Size.operator-, Size.operator-(const Size&), Size.operator-sub, Size::operator-, Size::operator-sub, _gdiplus_CLASS_Size_operator_opminus_sz_, gdiplus._gdiplus_CLASS_Size_operator_opminus_sz_, operator-, operator- method [GDI+], operator- method [GDI+],Size class
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Size::operator-
 - gdiplustypes/Size::operator-
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
 - Size.operator-
---

# Size::operator-sub


## -description

The <b>Size::operator-</b> method subtracts the <b>Width</b> and <b>Height</b> data members of two <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a> objects.

## -parameters

### -param sz [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a></b>

Reference to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a> object whose <b>Width</b> and <b>Height</b> data members are subtracted from the <b>Width</b> and <b>Height</b> data members of this <b>Size</b> object.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a></b>

This method returns the difference of this <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a> object and another <b>Size</b> object.

## -remarks

This method overloads the subtraction operator for <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a> objects. If A, B, and C are <b>Size</b> objects, the statement <b>C = A - B</b> is equivalent to <b>C = A.operator-(B)</b>.


#### Examples




```cpp
VOID Example_OperatorMinus(HWND hWnd)
{
   Graphics graphics(hdc);
   Pen pen(Color(255, 0, 0, 0));

   Size size1(200, 100);
   Size size2(50, 40);
   
   Size size3 = size1 - size2;

   graphics.DrawRectangle(&pen, 50, 50, size1.Width, size1.Height);
   graphics.DrawRectangle(&pen, 50, 50, size2.Width, size2.Height);
   graphics.DrawRectangle(&pen, 50, 50, size3.Width, size3.Height);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a>



<a href="/previous-versions/ms534751(v=vs.85)">Size::operator+</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-sizef">SizeF</a>