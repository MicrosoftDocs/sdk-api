---
UID: NF:vfw.DrawDibUpdate
title: DrawDibUpdate macro (vfw.h)
description: The DrawDibUpdate macro draws the last frame in the DrawDib off-screen buffer.
helpviewer_keywords: ["DrawDibUpdate","DrawDibUpdate macro [Windows Multimedia]","_win32_DrawDibUpdate","multimedia.drawdibupdate","vfw/DrawDibUpdate"]
old-location: multimedia\drawdibupdate.htm
tech.root: Multimedia
ms.assetid: 049a513a-bae1-4551-8700-cef417ed5373
ms.date: 07/01/2025
ms.keywords: DrawDibUpdate, DrawDibUpdate macro [Windows Multimedia], _win32_DrawDibUpdate, multimedia.drawdibupdate, vfw/DrawDibUpdate
req.header: vfw.h
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
 - DrawDibUpdate
 - vfw/DrawDibUpdate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - DrawDibUpdate
---

# DrawDibUpdate macro

## -syntax

```cpp
BOOL DrawDibUpdate(
    HDRAWDIB hdd,
    HDC hdc,
    int x,
    int y
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** otherwise.


## -description

The <b>DrawDibUpdate</b> macro draws the last frame in the DrawDib off-screen buffer.

## -parameters

### -param hdd

Handle to a DrawDib DC.

### -param hdc

Handle of the DC.

### -param x

The x-coordinate, in MM_TEXT client coordinates, of the upper left corner of the destination rectangle.

### -param y

The y-coordinate, in MM_TEXT client coordinates, of the upper left corner of the destination rectangle.

## -remarks

The <b>DrawDibUpdate</b> macro is defined as follows:


```cpp

#define DrawDibUpdate( hdd, hdc, x, y) \ 
    DrawDibDraw( hdd, hdc, x, y, 0, 0, NULL, NULL, 0, 0, \ 
    0, 0, DDF_UPDATE) 

```


This macro can be used to refresh an image or a portion of an image displayed by your application.

## -see-also

<a href="/windows/desktop/Multimedia/drawdib-macros">DrawDib Macros</a>
