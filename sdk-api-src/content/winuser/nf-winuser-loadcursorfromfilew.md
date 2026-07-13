---
UID: NF:winuser.LoadCursorFromFileW
title: LoadCursorFromFileW function (winuser.h)
description: Creates a cursor based on data contained in a file. (Unicode)
helpviewer_keywords: ["LoadCursorFromFile", "LoadCursorFromFile function [Menus and Other Resources]", "LoadCursorFromFileW", "_win32_LoadCursorFromFile", "_win32_loadcursorfromfile_cpp", "menurc.loadcursorfromfile", "winui._win32_loadcursorfromfile", "winuser/LoadCursorFromFile", "winuser/LoadCursorFromFileW"]
old-location: menurc\loadcursorfromfile.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\loadcursorfromfile.htm
ms.date: 12/05/2018
ms.keywords: LoadCursorFromFile, LoadCursorFromFile function [Menus and Other Resources], LoadCursorFromFileA, LoadCursorFromFileW, _win32_LoadCursorFromFile, _win32_loadcursorfromfile_cpp, menurc.loadcursorfromfile, winui._win32_loadcursorfromfile, winuser/LoadCursorFromFile, winuser/LoadCursorFromFileA, winuser/LoadCursorFromFileW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LoadCursorFromFileW (Unicode) and LoadCursorFromFileA (ANSI)
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
 - LoadCursorFromFileW
 - winuser/LoadCursorFromFileW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - ext-ms-win-ntuser-gui-l1-2-1.dll
api_name:
 - LoadCursorFromFile
 - LoadCursorFromFileA
 - LoadCursorFromFileW
---

# LoadCursorFromFileW function


## -description

Creates a cursor based on data contained in a file.

> [!NOTE]
> This function has been superseded by the [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagew) function (with **LR_DEFAULTSIZE** and **LR_LOADFROMFILE** flags set).

## -parameters

### -param lpFileName [in]

Type: <b>LPCTSTR</b>

The source of the file data to be used to create the cursor. The data in the file must be in either .CUR or .ANI format.

If the high-order word of <i>lpFileName</i> is nonzero, it is a pointer to a string that is a fully qualified name of a file containing cursor data.

## -returns

Type: <b>HCURSOR</b>

If the function is successful, the return value is a handle to the new cursor.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. <b>GetLastError</b> may return the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified file cannot be found.

</td>
</tr>
</table>

## -remarks

<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. The output returned is not affected by the DPI of the calling thread.

> [!NOTE]
> The winuser.h header defines LoadCursorFromFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>

<a href="/windows/desktop/menurc/cursors">Cursors</a>

<a href="/windows/desktop/api/winuser/nf-winuser-loadcursora">LoadCursor</a>

<b>Reference</b>

<a href="/windows/desktop/api/winuser/nf-winuser-setcursor">SetCursor</a>

<a href="/windows/desktop/api/winuser/nf-winuser-setsystemcursor">SetSystemCursor</a>
