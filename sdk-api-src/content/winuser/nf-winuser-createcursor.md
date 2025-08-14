---
UID: NF:winuser.CreateCursor
title: CreateCursor function (winuser.h)
description: Creates a cursor having the specified size, bit patterns, and hot spot.
helpviewer_keywords: ["CreateCursor","CreateCursor function [Menus and Other Resources]","_win32_CreateCursor","_win32_createcursor_cpp","menurc.createcursor","winui._win32_createcursor","winuser/CreateCursor"]
old-location: menurc\createcursor.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\createcursor.htm
ms.date: 12/05/2018
ms.keywords: CreateCursor, CreateCursor function [Menus and Other Resources], _win32_CreateCursor, _win32_createcursor_cpp, menurc.createcursor, winui._win32_createcursor, winuser/CreateCursor
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateCursor
 - winuser/CreateCursor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-gui-l1-3-1.dll
 - ext-ms-win-ntuser-gui-l1-3-0.dll
 - ext-ms-win-ntuser-gui-l1-2-0.dll
 - ext-ms-win-ntuser-gui-l1-1-1.dll
 - ext-ms-win-ntuser-gui-l1-1-0.dll
 - User32.dll
api_name:
 - CreateCursor
---

# CreateCursor function


## -description

Creates a monochrome cursor having the specified size, bit patterns, and hot spot.

To create a colored cursor at run time you can use the [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) function, which creates a cursor based on the content of an [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) structure.

## -parameters

### -param hInst [in, optional]

Type: <b>HINSTANCE</b>

A handle to the current instance of the application creating the cursor.

### -param xHotSpot [in]

Type: <b>int</b>

The horizontal position of the cursor's hot spot.

### -param yHotSpot [in]

Type: <b>int</b>

The vertical position of the cursor's hot spot.

### -param nWidth [in]

Type: <b>int</b>

The width of the cursor, in pixels.

### -param nHeight [in]

Type: <b>int</b>

The height of the cursor, in pixels.

### -param pvANDPlane [in]

Type: <b>const VOID*</b>

An array of bytes that contains the bit values for the AND mask of the cursor, as in a monochrome bitmap. See remarks.

### -param pvXORPlane [in]

Type: <b>const VOID*</b>

An array of bytes that contains the bit values for the XOR mask of the cursor, as in a monochrome bitmap. See remarks.

## -returns

Type: <b>HCURSOR</b>

If the function succeeds, the return value is a handle to the cursor.

If the function fails, the return value is **NULL**. To get extended error information, call [GetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

To determine the nominal size of a cursor, use the [GetSystemMetrics](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function, specifying the **SM_CXCURSOR** or **SM_CYCURSOR** value. Also, you can use the DPI-aware version of this API, see [GetSystemMetricsForDpi](/windows/win32/api/winuser/nf-winuser-getsystemmetricsfordpi). For more information see [High DPI Desktop Application Development on Windows](/windows/win32/hidpi/high-dpi-desktop-application-development-on-windows). 

For more information about _pvANDPlane_ and _pvXORPlane_ parameters see description of _lpBits_ parameter of [CreateBitmap](/windows/win32/api/wingdi/nf-wingdi-createbitmap) function.

**CreateCursor** applies the following truth table to the AND and XOR bitmasks:

| AND bitmask | XOR bitmask | Display |
|:-:|:-:|:-:|
| 0 | 0 | Black |
| 0 | 1 | White |
| 1 | 0 | Screen |
| 1 | 1 | Reverse screen |

Before closing, an application must call the [DestroyCursor](/windows/desktop/api/winuser/nf-winuser-destroycursor) function to free any system resources associated with the cursor.

<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. The output returned is in terms of physical coordinates, and  is not affected by the DPI of the calling thread. Note that the cursor created may still be scaled to match the DPI of any given window it is drawn into.

#### Examples

For an example, see [Creating a Cursor](/windows/desktop/menurc/using-cursors).

## -see-also

[CreateIcon](/windows/desktop/api/winuser/nf-winuser-createicon)

[CreateIconIndirect](/windows/desktop/api/Winuser/nf-winuser-createiconindirect)

[DestroyCursor](/windows/desktop/api/winuser/nf-winuser-destroycursor)

[GetSystemMetrics](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)

[SetCursor](/windows/desktop/api/winuser/nf-winuser-setcursor)

[Cursors](/windows/desktop/menurc/cursors)
