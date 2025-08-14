---
UID: NF:winuser.LoadCursorW
title: LoadCursorW function (winuser.h)
description: Loads the specified cursor resource from the executable (.EXE) file associated with an application instance. (Unicode)
helpviewer_keywords: ["LoadCursor", "LoadCursor function [Menus and Other Resources]", "LoadCursorW", "_win32_LoadCursor", "_win32_loadcursor_cpp", "menurc.loadcursor", "winui._win32_loadcursor", "winuser/LoadCursor", "winuser/LoadCursorW"]
old-location: menurc\loadcursor.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\loadcursor.htm
ms.date: 12/05/2018
ms.keywords: LoadCursor, LoadCursor function [Menus and Other Resources], LoadCursorA, LoadCursorW, _win32_LoadCursor, _win32_loadcursor_cpp, menurc.loadcursor, winui._win32_loadcursor, winuser/LoadCursor, winuser/LoadCursorA, winuser/LoadCursorW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LoadCursorW (Unicode) and LoadCursorA (ANSI)
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
 - LoadCursorW
 - winuser/LoadCursorW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-cursor-l1-1-1.dll
 - User32.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-0.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-1.dll
 - Ext-MS-Win-NTUser-GUI-l1-2-0.dll
 - api-ms-win-ntuser-ie-gui-l1-1-0.dll
 - ie_stubs.dll
 - ext-ms-win-ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-RTCore-NTUser-Cursor-L1-1-0.dll
 - MinUser.dll
api_name:
 - LoadCursor
 - LoadCursorA
 - LoadCursorW
---

# LoadCursorW function


## -description

Loads the specified cursor resource from the executable (.exe) file associated with an application instance.

> [!NOTE]
> This function has been superseded by the [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagew) function (with **LR_DEFAULTSIZE** and **LR_SHARED** flags set).

## -parameters

### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the module of either a DLL or executable (.exe) file that contains the cursor to be loaded. For more information, see <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a>.

To load a predefined system cursor, set this parameter to <b>NULL</b>.
### -param lpCursorName [in]

Type: <b>LPCTSTR</b>

If <i>hInstance</i> is non-<b>NULL</b>, <i>lpCursorName</i> specifies the cursor resource either by name or ordinal. This ordinal must be packaged by using the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcew">MAKEINTRESOURCE</a> macro.

If <i>hInstance</i> is <b>NULL</b>, <i>lpCursorName</i> specifies the identifier that begins with the [IDC\_ prefix](/windows/win32/menurc/about-cursors) of a predefined system cursor to load.

## -returns

Type: <b>HCURSOR</b>

If the function succeeds, the return value is the handle to the newly loaded cursor.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>LoadCursor</b> function loads the cursor resource only if it has not been loaded; otherwise, it retrieves the handle to the existing resource. This function returns a valid cursor handle only if the <i>lpCursorName</i> parameter is a pointer to a cursor resource. If <i>lpCursorName</i> is a pointer to any type of resource other than a cursor (such as an icon), the return value is not <b>NULL</b>, even though it is not a valid cursor handle. 

The <b>LoadCursor</b> function searches the cursor resource most appropriate for the cursor for the current display device. The cursor resource can be a color or monochrome bitmap. 

<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. The output returned is not affected by the DPI of the calling thread.

#### Examples

For an example, see <a href="/windows/desktop/menurc/using-cursors">Creating a Cursor</a>.

> [!NOTE]
> The winuser.h header defines LoadCursor as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>

<a href="/windows/desktop/menurc/cursors">Cursors</a>

<a href="/windows/desktop/api/winuser/nf-winuser-loadimagea">LoadImage</a>

<a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>

<a href="/windows/win32/api/winuser/nf-winuser-is_intresource">IS_INTRESOURCE</a>

<b>Reference</b>

<a href="/windows/desktop/api/winuser/nf-winuser-setcursor">SetCursor</a>

<a href="/windows/desktop/api/winuser/nf-winuser-setcursorpos">SetCursorPos</a>

<a href="/windows/desktop/api/winuser/nf-winuser-showcursor">ShowCursor</a>
