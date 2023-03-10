---
UID: NF:gdiplustypes.SizeF.operator-add
title: SizeF::operator-add (gdiplustypes.h)
description: The SizeF::operator+ method adds the Width and Height data members of two SizeF objects.
helpviewer_keywords: ["SizeF class [GDI+]","operator+ method","SizeF.operator+","SizeF.operator+(const SizeF&)","SizeF.operator-add","SizeF::operator+","SizeF::operator-add","_gdiplus_CLASS_SizeF_operator_opadd_sz_","gdiplus._gdiplus_CLASS_SizeF_operator_opadd_sz_","operator+","operator+ method [GDI+]","operator+ method [GDI+]","SizeF class"]
old-location: gdiplus\_gdiplus_CLASS_SizeF_operator_opadd_sz_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\sizefclass\sizefmethods\operatorplus_93sz.htm
ms.date: 12/05/2018
ms.keywords: SizeF class [GDI+],operator+ method, SizeF.operator+, SizeF.operator+(const SizeF&), SizeF.operator-add, SizeF::operator+, SizeF::operator-add, _gdiplus_CLASS_SizeF_operator_opadd_sz_, gdiplus._gdiplus_CLASS_SizeF_operator_opadd_sz_, operator+, operator+ method [GDI+], operator+ method [GDI+],SizeF class
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
 - SizeF::operator+
 - gdiplustypes/SizeF::operator+
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
 - SizeF.operator+
---

# SizeF::operator-add


## -description

The <b>SizeF::operator+</b> method adds the <b>Width</b> and <b>Height</b> data members of two <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-sizef">SizeF</a> objects.

## -parameters

### -param sz [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-sizef">SizeF</a></b>

Reference to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-sizef">SizeF</a> object whose <b>Width</b> and <b>Height</b> data members are added to the <b>Width</b> and <b>Height</b> data members of this <b>SizeF</b> object.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-sizef">SizeF</a></b>

This method returns the sum of this <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-sizef">SizeF</a> object and another <b>SizeF</b> object.

## -remarks

This method overloads the addition operator for 
				<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-sizef">SizeF</a> objects. If A, B, and C are 
				<b>SizeF</b> objects, the statement <b>C = A + B</b> is equivalent to <b>C = A.operator+(B)</b>.


#### Examples




```cpp
VOID Example_OperatorPlus(HDC hdc)
{

   Graphics graphics(hdc);
   Pen pen(Color(255, 0, 0, 0));

   SizeF size1(80.0f, 30.0f);
   SizeF size2(50.0f, 20.0f);
   
   SizeF size3 = size1 + size2;

   graphics.DrawRectangle(&pen, 50.0f, 50.0f, size1.Width, size1.Height);
   graphics.DrawRectangle(&pen, 50.0f, 50.0f, size2.Width, size2.Height);
   graphics.DrawRectangle(&pen, 50.0f, 50.0f, size3.Width, size3.Height);

}
```

## -see-also

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-sizef">SizeF</a>



<a href="/previous-versions/ms534743(v=vs.85)">SizeF::operator-</a>