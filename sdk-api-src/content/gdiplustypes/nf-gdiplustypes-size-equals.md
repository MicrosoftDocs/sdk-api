---
UID: NF:gdiplustypes.Size.Equals
title: Size::Equals (gdiplustypes.h)
description: The Size::Equals method determines whether two Size objects are equal.
helpviewer_keywords: ["Equals","Equals method [GDI+]","Equals method [GDI+]","Size class","Size class [GDI+]","Equals method","Size.Equals","Size::Equals","_gdiplus_CLASS_Size_Equals_sz_","gdiplus._gdiplus_CLASS_Size_Equals_sz_"]
old-location: gdiplus\_gdiplus_CLASS_Size_Equals_sz_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\sizeclass\sizemethods\equals_53sz.htm
ms.date: 12/05/2018
ms.keywords: Equals, Equals method [GDI+], Equals method [GDI+],Size class, Size class [GDI+],Equals method, Size.Equals, Size::Equals, _gdiplus_CLASS_Size_Equals_sz_, gdiplus._gdiplus_CLASS_Size_Equals_sz_
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
 - Size::Equals
 - gdiplustypes/Size::Equals
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
 - Size.Equals
---

# Size::Equals


## -description

The <b>Size::Equals</b> method determines whether two 
			<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a> objects are equal.

## -parameters

### -param sz [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a></b>

Reference to a 
					<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a> object that is compared to this 
					<b>Size</b> object.

## -returns

Type: <b>BOOL</b>

If the 
						<b>Width</b> and 
						<b>Height</b>  data members of the two 
						<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a> objects are equal, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.

## -remarks

Two 
				<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a> objects are defined as equal if the 
				<b>Width</b> and 
				<b>Height</b>  data members are equal.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a> object, gets the size of the rectangle, and determines whether the rectangles are equal.


```cpp
Rect rect(50, 30, 200, 100);
Size desiredSize(200, 100);
Size rectSize;

// Get the size of the rectangle.
rect.GetSize(&rectSize);

if(rectSize.Equals(desiredSize))
{
   // The rectangle has the desired size.
} 
```

## -see-also

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-sizef">SizeF</a>