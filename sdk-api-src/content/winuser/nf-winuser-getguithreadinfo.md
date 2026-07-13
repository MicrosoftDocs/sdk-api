---
UID: NF:winuser.GetGUIThreadInfo
title: GetGUIThreadInfo function (winuser.h)
description: Retrieves information about the active window or a specified GUI thread.
helpviewer_keywords: ["GetGUIThreadInfo","GetGUIThreadInfo function [Windows and Messages]","_win32_GetGUIThreadInfo","_win32_getguithreadinfo_cpp","winmsg.getguithreadinfo","winui._win32_getguithreadinfo","winuser/GetGUIThreadInfo"]
old-location: winmsg\getguithreadinfo.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getguithreadinfo.htm
ms.date: 12/05/2018
ms.keywords: GetGUIThreadInfo, GetGUIThreadInfo function [Windows and Messages], _win32_GetGUIThreadInfo, _win32_getguithreadinfo_cpp, winmsg.getguithreadinfo, winui._win32_getguithreadinfo, winuser/GetGUIThreadInfo
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
 - GetGUIThreadInfo
 - winuser/GetGUIThreadInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-window-ext-l1-1-1.dll
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - minuser.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetGUIThreadInfo
req.apiset: ext-ms-win-ntuser-window-l1-1-1 (introduced in Windows 8.1)
---

# GetGUIThreadInfo function


## -description

Retrieves information about the active window or a specified GUI thread.

## -parameters

### -param idThread [in]

Type: <b>DWORD</b>

The identifier for the thread for which information is to be retrieved. To retrieve this value, use the <a href="/windows/desktop/api/winuser/nf-winuser-getwindowthreadprocessid">GetWindowThreadProcessId</a> function. If this parameter is <b>NULL</b>, the function returns information for the foreground thread.

### -param pgui [in, out]

Type: <b>LPGUITHREADINFO</b>

A pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-guithreadinfo">GUITHREADINFO</a> structure that receives information describing the thread. Note that you must set the <b>cbSize</b> member to <code>sizeof(GUITHREADINFO)</code> before calling this function.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function succeeds even if the active window is not owned by the calling process. If the specified thread does not exist or have an input queue, the function will fail. 

This function is useful for retrieving out-of-context information about a thread. The information retrieved is the same as if an application retrieved the information about itself. 

For an edit control, the returned <b>rcCaret</b> rectangle contains the caret plus information on text direction and padding. Thus, it may not give the correct position of the cursor. The Sans Serif font uses four characters for the cursor: 
				

<table class="clsStd">
<tr>
<th>Cursor character</th>
<th>Unicode code point</th>
</tr>
<tr>
<td><b>CURSOR_LTR</b></td>
<td>0xf00c</td>
</tr>
<tr>
<td><b>CURSOR_RTL</b></td>
<td>0xf00d</td>
</tr>
<tr>
<td><b>CURSOR_THAI</b></td>
<td>0xf00e</td>
</tr>
<tr>
<td><b>CURSOR_USA</b></td>
<td>0xfff (this is a marker value with no associated glyph)</td>
</tr>
</table>
 

 To get the actual insertion point in the <b>rcCaret</b> rectangle, perform the following steps.
				<ol>
<li>Call <a href="/windows/desktop/api/winuser/nf-winuser-getkeyboardlayout">GetKeyboardLayout</a> to retrieve the current input language. </li>
<li>Determine the character used for the cursor, based on the current input language.</li>
<li>Call <a href="/windows/desktop/api/wingdi/nf-wingdi-createfonta">CreateFont</a> using Sans Serif for the font, the height given by <b>rcCaret</b>, and a width of <code>zero</code>. For <i>fnWeight</i>, call <code>SystemParametersInfo(SPI_GETCARETWIDTH, 0, pvParam, 0)</code>. If <i>pvParam</i> is greater than 1, set <i>fnWeight</i> to 700, otherwise set <i>fnWeight</i> to 400.</li>
<li>Select the font into a device context (DC) and use <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharabcwidthsa">GetCharABCWidths</a> to get the <code>B</code> width of the appropriate cursor character.</li>
<li>Add the <code>B</code> width to <b>rcCaret</b>.<b>left</b> to obtain the actual insertion point.</li>
</ol>


The function may not return valid window handles in the <a href="/windows/desktop/api/winuser/ns-winuser-guithreadinfo">GUITHREADINFO</a> structure when called to retrieve information for the foreground thread, such as when a window is losing activation.





<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
The coordinates returned in the <b>rcCaret</b> rect of the <a href="/windows/desktop/api/winuser/ns-winuser-guithreadinfo">GUITHREADINFO</a> struct are logical coordinates in terms of the window associated with the caret. They are not virtualized into the mode of the calling thread.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/ns-winuser-guithreadinfo">GUITHREADINFO</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getcursorinfo">GetCursorInfo</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getwindowthreadprocessid">GetWindowThreadProcessId</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/windows">Windows</a>
