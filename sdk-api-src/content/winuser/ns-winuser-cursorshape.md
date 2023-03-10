---
UID: NS:winuser.tagCURSORSHAPE
title: CURSORSHAPE (winuser.h)
description: Contains information about a cursor.
helpviewer_keywords: ["*LPCURSORSHAPE","CURSORSHAPE","CURSORSHAPE structure [Menus and Other Resources]","LPCURSORSHAPE","LPCURSORSHAPE structure pointer [Menus and Other Resources]","_win32_CURSORSHAPE_str","_win32_cursorshape_str_cpp","menurc.cursorshape","winui._win32_cursorshape_str","winuser/CURSORSHAPE","winuser/LPCURSORSHAPE"]
old-location: menurc\cursorshape.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcestructures\cursorshape.htm
ms.date: 12/05/2018
ms.keywords: '*LPCURSORSHAPE, CURSORSHAPE, CURSORSHAPE structure [Menus and Other Resources], LPCURSORSHAPE, LPCURSORSHAPE structure pointer [Menus and Other Resources], _win32_CURSORSHAPE_str, _win32_cursorshape_str_cpp, menurc.cursorshape, winui._win32_cursorshape_str, winuser/CURSORSHAPE, winuser/LPCURSORSHAPE'
req.header: winuser.h
req.include-header: Windows.h
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
req.typenames: CURSORSHAPE, *LPCURSORSHAPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCURSORSHAPE
 - winuser/tagCURSORSHAPE
 - LPCURSORSHAPE
 - winuser/LPCURSORSHAPE
 - CURSORSHAPE
 - winuser/CURSORSHAPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - CURSORSHAPE
---

# CURSORSHAPE structure


## -description

Contains information about a cursor.

## -struct-fields

### -field xHotSpot

Type: <b>int</b>

The horizontal position of the hot spot, relative to the upper-left corner of the cursor bitmap.

### -field yHotSpot

Type: <b>int</b>

The vertical position of the hot spot, relative to the upper-left corner of the cursor bitmap.

### -field cx

Type: <b>int</b>

The width, in pixels, of the cursor.

### -field cy

Type: <b>int</b>

The height, in pixels, of the cursor.

### -field cbWidth

Type: <b>int</b>

The width, in bytes, of the cursor bitmap.

### -field Planes

Type: <b>BYTE</b>

The number of color planes.

### -field BitsPixel

Type: <b>BYTE</b>

The number of bits used to indicate the color of a single pixel in the cursor.

## -remarks

When an application passes a cursor handle to the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-lockresource">LockResource</a> function, the function returns a pointer to a buffer containing information about the cursor. An application can use the <b>CURSORSHAPE</b> structure to access the information.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-lockresource">LockResource</a>



<b>Reference</b>



<a href="/windows/desktop/menurc/resources">Resources</a>