---
UID: NF:winuser.LoadCursorW
title: LoadCursorW function (winuser.h)
description: Loads the specified cursor resource from the executable (.EXE) file associated with an application instance. (Unicode)
helpviewer_keywords: ["IDC_APPSTARTING", "IDC_ARROW", "IDC_CROSS", "IDC_HAND", "IDC_HELP", "IDC_IBEAM", "IDC_ICON", "IDC_NO", "IDC_SIZE", "IDC_SIZEALL", "IDC_SIZENESW", "IDC_SIZENS", "IDC_SIZENWSE", "IDC_SIZEWE", "IDC_UPARROW", "IDC_WAIT", "LoadCursor", "LoadCursor function [Menus and Other Resources]", "LoadCursorW", "_win32_LoadCursor", "_win32_loadcursor_cpp", "menurc.loadcursor", "winui._win32_loadcursor", "winuser/LoadCursor", "winuser/LoadCursorW"]
old-location: menurc\loadcursor.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\loadcursor.htm
ms.date: 12/05/2018
ms.keywords: IDC_APPSTARTING, IDC_ARROW, IDC_CROSS, IDC_HAND, IDC_HELP, IDC_IBEAM, IDC_ICON, IDC_NO, IDC_SIZE, IDC_SIZEALL, IDC_SIZENESW, IDC_SIZENS, IDC_SIZENWSE, IDC_SIZEWE, IDC_UPARROW, IDC_WAIT, LoadCursor, LoadCursor function [Menus and Other Resources], LoadCursorA, LoadCursorW, _win32_LoadCursor, _win32_loadcursor_cpp, menurc.loadcursor, winui._win32_loadcursor, winuser/LoadCursor, winuser/LoadCursorA, winuser/LoadCursorW
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

Loads the specified cursor resource from the executable (.EXE) file associated with an application instance.

> [!NOTE]
> This function has been superseded by the [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagew) function (with **LR_DEFAULTSIZE** and **LR_SHARED** flags set).

## -parameters

### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to an instance of the module whose executable file contains the cursor to be loaded.

### -param lpCursorName [in]

Type: <b>LPCTSTR</b>

The name of the cursor resource to be loaded. Alternatively, this parameter can consist of the resource identifier in the low-order word and zero in the high-order word. The <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro can also be used to create this value. To use one of the predefined cursors, the application must set the <i>hInstance</i> parameter to <b>NULL</b> and the <i>lpCursorName</i> parameter to one the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IDC_APPSTARTING"></a><a id="idc_appstarting"></a><dl>
<dt><b>IDC_APPSTARTING</b></dt>
<dt>MAKEINTRESOURCE(32650)</dt>
</dl>
</td>
<td width="60%">
Standard arrow and small hourglass

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_ARROW"></a><a id="idc_arrow"></a><dl>
<dt><b>IDC_ARROW</b></dt>
<dt>MAKEINTRESOURCE(32512)</dt>
</dl>
</td>
<td width="60%">
Standard arrow

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_CROSS"></a><a id="idc_cross"></a><dl>
<dt><b>IDC_CROSS</b></dt>
<dt>MAKEINTRESOURCE(32515)</dt>
</dl>
</td>
<td width="60%">
Crosshair

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_HAND"></a><a id="idc_hand"></a><dl>
<dt><b>IDC_HAND</b></dt>
<dt>MAKEINTRESOURCE(32649)</dt>
</dl>
</td>
<td width="60%">
 Hand

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_HELP"></a><a id="idc_help"></a><dl>
<dt><b>IDC_HELP</b></dt>
<dt>MAKEINTRESOURCE(32651)</dt>
</dl>
</td>
<td width="60%">
Arrow and question mark

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_IBEAM"></a><a id="idc_ibeam"></a><dl>
<dt><b>IDC_IBEAM</b></dt>
<dt>MAKEINTRESOURCE(32513)</dt>
</dl>
</td>
<td width="60%">
I-beam

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_ICON"></a><a id="idc_icon"></a><dl>
<dt><b>IDC_ICON</b></dt>
<dt>MAKEINTRESOURCE(32641)</dt>
</dl>
</td>
<td width="60%">
Obsolete for applications marked version 4.0 or later.

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_NO"></a><a id="idc_no"></a><dl>
<dt><b>IDC_NO</b></dt>
<dt>MAKEINTRESOURCE(32648)</dt>
</dl>
</td>
<td width="60%">
Slashed circle

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_SIZE"></a><a id="idc_size"></a><dl>
<dt><b>IDC_SIZE</b></dt>
<dt>MAKEINTRESOURCE(32640)</dt>
</dl>
</td>
<td width="60%">
Obsolete for applications marked version 4.0 or later. Use <b>IDC_SIZEALL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_SIZEALL"></a><a id="idc_sizeall"></a><dl>
<dt><b>IDC_SIZEALL</b></dt>
<dt>MAKEINTRESOURCE(32646)</dt>
</dl>
</td>
<td width="60%">
Four-pointed arrow pointing north, south, east, and west

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_SIZENESW"></a><a id="idc_sizenesw"></a><dl>
<dt><b>IDC_SIZENESW</b></dt>
<dt>MAKEINTRESOURCE(32643)</dt>
</dl>
</td>
<td width="60%">
Double-pointed arrow pointing northeast and southwest

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_SIZENS"></a><a id="idc_sizens"></a><dl>
<dt><b>IDC_SIZENS</b></dt>
<dt>MAKEINTRESOURCE(32645)</dt>
</dl>
</td>
<td width="60%">
Double-pointed arrow pointing north and south

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_SIZENWSE"></a><a id="idc_sizenwse"></a><dl>
<dt><b>IDC_SIZENWSE</b></dt>
<dt>MAKEINTRESOURCE(32642)</dt>
</dl>
</td>
<td width="60%">
Double-pointed arrow pointing northwest and southeast

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_SIZEWE"></a><a id="idc_sizewe"></a><dl>
<dt><b>IDC_SIZEWE</b></dt>
<dt>MAKEINTRESOURCE(32644)</dt>
</dl>
</td>
<td width="60%">
Double-pointed arrow pointing west and east

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_UPARROW"></a><a id="idc_uparrow"></a><dl>
<dt><b>IDC_UPARROW</b></dt>
<dt>MAKEINTRESOURCE(32516)</dt>
</dl>
</td>
<td width="60%">
Vertical arrow

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_WAIT"></a><a id="idc_wait"></a><dl>
<dt><b>IDC_WAIT</b></dt>
<dt>MAKEINTRESOURCE(32514)</dt>
</dl>
</td>
<td width="60%">
Hourglass

</td>
</tr>
</table>

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

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines LoadCursor as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/menurc/cursors">Cursors</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadimagea">LoadImage</a>



<a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setcursor">SetCursor</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setcursorpos">SetCursorPos</a>



<a href="/windows/desktop/api/winuser/nf-winuser-showcursor">ShowCursor</a>
