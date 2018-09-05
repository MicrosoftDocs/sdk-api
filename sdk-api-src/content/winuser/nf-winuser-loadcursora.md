---
UID: NF:winuser.LoadCursorA
title: LoadCursorA function
author: windows-sdk-content
description: Loads the specified cursor resource from the executable (.EXE) file associated with an application instance.
old-location: menurc\loadcursor.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\loadcursor.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IDC_APPSTARTING, IDC_ARROW, IDC_CROSS, IDC_HAND, IDC_HELP, IDC_IBEAM, IDC_ICON, IDC_NO, IDC_SIZE, IDC_SIZEALL, IDC_SIZENESW, IDC_SIZENS, IDC_SIZENWSE, IDC_SIZEWE, IDC_UPARROW, IDC_WAIT, LoadCursor, LoadCursor function [Menus and Other Resources], LoadCursorA, LoadCursorW, _win32_LoadCursor, _win32_loadcursor_cpp, menurc.loadcursor, winui._win32_loadcursor, winuser/LoadCursor, winuser/LoadCursorA, winuser/LoadCursorW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: 
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
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# LoadCursorA function


## -description


Loads the specified cursor resource from the executable (.EXE) file associated with an application instance.
<div class="alert"><b>Note</b>  This function has been superseded by the <a href="https://msdn.microsoft.com/27a18763-60e0-4a91-9262-807ea2b67416">LoadImage</a> function.</div><div> </div>

## -parameters




### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to an instance of the module whose executable file contains the cursor to be loaded. 


### -param lpCursorName [in]

Type: <b>LPCTSTR</b>

The name of the cursor resource to be loaded. Alternatively, this parameter can consist of the resource identifier in the low-order word and zero in the high-order word. The <a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a> macro can also be used to create this value. To use one of the predefined cursors, the application must set the <i>hInstance</i> parameter to <b>NULL</b> and the <i>lpCursorName</i> parameter to one the following values.

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

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The <b>LoadCursor</b> function loads the cursor resource only if it has not been loaded; otherwise, it retrieves the handle to the existing resource. This function returns a valid cursor handle only if the <i>lpCursorName</i> parameter is a pointer to a cursor resource. If <i>lpCursorName</i> is a pointer to any type of resource other than a cursor (such as an icon), the return value is not <b>NULL</b>, even though it is not a valid cursor handle. 

The <b>LoadCursor</b> function searches the cursor resource most appropriate for the cursor for the current display device. The cursor resource can be a color or monochrome bitmap. 

<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. The output returned is not affected by the DPI of the calling thread.


#### Examples

For an example, see <a href="using_cursors.htm">Creating a Cursor</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/d24e21f2-224d-4f32-aa0b-70844e3628ad">Cursors</a>



<a href="https://msdn.microsoft.com/27a18763-60e0-4a91-9262-807ea2b67416">LoadImage</a>



<a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/69bb9f90-5366-4141-97b6-57e41b774614">SetCursor</a>



<a href="https://msdn.microsoft.com/b17cf57f-dd96-4695-a51e-ee1e1f00f85f">SetCursorPos</a>



<a href="https://msdn.microsoft.com/6712b6b7-bdb0-4078-ba38-7ad744bbf765">ShowCursor</a>
 

 

