---
UID: NF:gdiplustypes.Size.Empty
title: Size::Empty (gdiplustypes.h)
description: The Size::Empty method determines whether a Size object is empty.
helpviewer_keywords: ["Empty","Empty method [GDI+]","Empty method [GDI+]","Size class","Size class [GDI+]","Empty method","Size.Empty","Size::Empty","_gdiplus_CLASS_Size_Empty_","gdiplus._gdiplus_CLASS_Size_Empty_"]
old-location: gdiplus\_gdiplus_CLASS_Size_Empty_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\sizeclass\sizemethods\empty.htm
ms.date: 12/05/2018
ms.keywords: Empty, Empty method [GDI+], Empty method [GDI+],Size class, Size class [GDI+],Empty method, Size.Empty, Size::Empty, _gdiplus_CLASS_Size_Empty_, gdiplus._gdiplus_CLASS_Size_Empty_
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
 - Size::Empty
 - gdiplustypes/Size::Empty
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
 - Size.Empty
---

# Size::Empty


## -description

The <b>Size::Empty</b> method determines whether a 
			<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a> object is empty.



## -returns

Type: <b>BOOL</b>

If the 
						<b>Width</b> and 
						<b>Height</b> data members are both equal to zero, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.

## -remarks

A 
				<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a> object is defined as empty if the 
				<b>Width</b> and 
				<b>Height</b> data members are both equal to zero.


#### Examples




```cpp
Rect rect(50, 50, 100, 200);
Size size;

rect.Inflate(-50, -100);
rect.GetSize(&size);

if(size.Empty())
{
   // The width and height are both 0.
}
```

## -see-also

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-sizef">SizeF</a>
