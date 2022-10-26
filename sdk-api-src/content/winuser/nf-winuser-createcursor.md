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

An array of bytes that contains the bit values for the AND mask of the cursor, as in a device-dependent monochrome bitmap.

### -param pvXORPlane [in]

Type: <b>const VOID*</b>

An array of bytes that contains the bit values for the XOR mask of the cursor, as in a device-dependent monochrome bitmap.

## -returns

Type: <b>HCURSOR</b>

If the function succeeds, the return value is a handle to the cursor.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <i>nWidth</i> and <i>nHeight</i> parameters must specify a width and height that are supported by the current display driver, because the system cannot create cursors of other sizes. To determine the width and height supported by the display driver, use the <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a> function, specifying the <b>SM_CXCURSOR</b> or <b>SM_CYCURSOR</b> value. 

Before closing, an application must call the <a href="/windows/desktop/api/winuser/nf-winuser-destroycursor">DestroyCursor</a> function to free any system resources associated with the cursor.

<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. The output returned is in terms of physical coordinates, and  is not affected by the DPI of the calling thread. Note that the cursor created may still be scaled to match the DPI of any given window it is drawn into.

#### Examples

For an example, see <a href="/windows/desktop/menurc/using-cursors">Creating a Cursor</a>.

## -see-also

<b>Conceptual</b>

<a href="/windows/desktop/api/winuser/nf-winuser-createicon">CreateIcon</a>

<a href="/windows/desktop/api/Winuser/nf-winuser-createiconindirect">CreateIconIndirect</a>

<a href="/windows/desktop/menurc/cursors">Cursors</a>

<a href="/windows/desktop/api/winuser/nf-winuser-destroycursor">DestroyCursor</a>

<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a>

<a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a>

<b>Other Resources</b>


<b>Reference</b>

<a href="/windows/desktop/api/winuser/nf-winuser-setcursor">SetCursor</a>
