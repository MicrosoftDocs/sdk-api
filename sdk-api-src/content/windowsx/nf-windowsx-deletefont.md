---
UID: NF:windowsx.DeleteFont
title: DeleteFont macro (windowsx.h)
description: The DeleteFont macro deletes a font object, freeing all system resources associated with the font object.
helpviewer_keywords: ["DeleteFont","DeleteFont macro [Windows GDI]","_win32_DeleteFont","gdi.deletefont","windowsx/DeleteFont"]
old-location: gdi\deletefont.htm
tech.root: gdi
ms.assetid: 5cb6c667-3c8b-41cf-b2b7-9e1e89729da7
ms.date: 07/01/2025
ms.keywords: DeleteFont, DeleteFont macro [Windows GDI], _win32_DeleteFont, gdi.deletefont, windowsx/DeleteFont
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
 - DeleteFont
 - windowsx/DeleteFont
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
 - DeleteFont
---

# DeleteFont macro

## -syntax

```cpp
BOOL DeleteFont(
    HFONT hfont
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

If **DeleteFont** succeeds, the return value is nonzero. If the specified handle is not valid or is currently selected into a Device Context, the return value is zero.


## -description

The <b>DeleteFont</b> macro deletes a font object, freeing all system resources associated with the font object.

## -parameters

### -param hfont

A handle to the font object.

## -remarks

After the font object is deleted, the specified handle is no longer valid.

The <b>DeleteFont</b> macro is equivalent to calling <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> as follows:


``` syntax

   DeleteObject((HGDIOBJ)(HFONT)(hfont))

```


## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<a href="/windows/desktop/api/windowsx/nf-windowsx-selectfont">SelectFont</a>
