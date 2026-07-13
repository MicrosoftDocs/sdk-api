---
UID: NF:windowsx.SelectFont
title: SelectFont macro (windowsx.h)
description: The SelectFont macro selects a font object into the specified device context (DC). The new font object replaces the previous font object.
helpviewer_keywords: ["SelectFont","SelectFont macro [Windows GDI]","_win32_SelectFont","gdi.selectfont","windowsx/SelectFont"]
old-location: gdi\selectfont.htm
tech.root: gdi
ms.assetid: e7c145aa-566d-4754-a4dd-a5e71e188258
ms.date: 07/01/2025
ms.keywords: SelectFont, SelectFont macro [Windows GDI], _win32_SelectFont, gdi.selectfont, windowsx/SelectFont
req.header: windowsx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SelectFont
 - windowsx/SelectFont
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windowsx.h
api_name:
 - SelectFont
---

# SelectFont macro

## -syntax

```cpp
HFONT SelectFont(
    HDC hdc,
    HFONT hfont
);
```

## -returns

Type: **[HFONT](/windows/desktop/winprog/windows-data-types)**

If **SelectFont** succeeds, the return value is a handle to the font object being replaced. If an error occurs, the return value is **NULL**.


## -description

The <b>SelectFont</b> macro selects a font object into the specified device context (DC). The new font object replaces the previous font object.

## -parameters

### -param hdc

A handle to the DC.

### -param hfont

A handle to the font object to be selected. The font object must have been created using either <a href="/windows/desktop/api/wingdi/nf-wingdi-createfonta">CreateFont</a> or <a href="/windows/desktop/api/wingdi/nf-wingdi-createfontindirecta">CreateFontIndirect</a>.

## -remarks

After an application has finished drawing with the new font object, it should always replace a new font object with the original font object.

The <b>SelectFont</b> macro is equivalent to calling <a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a> as follows:


``` syntax

((HFONT) SelectObject((hdc), (HGDIOBJ)(HFONT)(hfont)))

```


## -see-also

<a href="/windows/desktop/api/windowsx/nf-windowsx-deletefont">DeleteFont</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>
