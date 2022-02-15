---
UID: NF:gdiplustypes.SizeF.Empty
title: SizeF::Empty (gdiplustypes.h)
description: The SizeF::Empty method determines whether a SizeF object is empty.
helpviewer_keywords: ["Empty","Empty method [GDI+]","Empty method [GDI+]","SizeF class","SizeF class [GDI+]","Empty method","SizeF.Empty","SizeF::Empty","_gdiplus_CLASS_SizeF_Empty_","gdiplus._gdiplus_CLASS_SizeF_Empty_"]
old-location: gdiplus\_gdiplus_CLASS_SizeF_Empty_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\sizefclass\sizefmethods\empty_16.htm
ms.date: 12/05/2018
ms.keywords: Empty, Empty method [GDI+], Empty method [GDI+],SizeF class, SizeF class [GDI+],Empty method, SizeF.Empty, SizeF::Empty, _gdiplus_CLASS_SizeF_Empty_, gdiplus._gdiplus_CLASS_SizeF_Empty_
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
 - SizeF::Empty
 - gdiplustypes/SizeF::Empty
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
 - SizeF.Empty
---

# SizeF::Empty


## -description

The <b>SizeF::Empty</b> method determines whether a 
			<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-sizef">SizeF</a> object is empty.



## -returns

Type: <b>BOOL</b>

If the 
						<b>Width</b> and 
						<b>Height</b> data members are both equal to zero, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.

## -remarks

A 
				<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-sizef">SizeF</a> object is defined as empty if the 
				<b>Width</b> and 
				<b>Height</b> data members are both equal to zero.


#### Examples




```cpp
RectF rect(50.0f, 50.0f, 100.0f, 200.0f);
SizeF size;

rect.Inflate(-50.0f, -100.0f);
rect.GetSize(&size);

if(size.Empty())
{

   // The width and height are both 0.
}
```

## -see-also

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-sizef">SizeF</a>
