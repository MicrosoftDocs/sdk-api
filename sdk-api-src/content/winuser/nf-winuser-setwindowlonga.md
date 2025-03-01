---
UID: NF:winuser.SetWindowLongA
title: SetWindowLongA function (winuser.h)
description: Changes an attribute of the specified window. The function also sets the 32-bit (long) value at the specified offset into the extra window memory. (ANSI)
helpviewer_keywords: ["DWL_DLGPROC", "DWL_MSGRESULT", "DWL_USER", "GWL_EXSTYLE", "GWL_HINSTANCE", "GWL_ID", "GWL_STYLE", "GWL_USERDATA", "GWL_WNDPROC", "SetWindowLongA", "winuser/SetWindowLongA"]
old-location: winmsg\setwindowlong.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowclasses\windowclassreference\windowclassfunctions\setwindowlong.htm
ms.date: 12/05/2018
ms.keywords: DWL_DLGPROC, DWL_MSGRESULT, DWL_USER, GWL_EXSTYLE, GWL_HINSTANCE, GWL_ID, GWL_STYLE, GWL_USERDATA, GWL_WNDPROC, SetWindowLong, SetWindowLong function [Windows and Messages], SetWindowLongA, SetWindowLongW, _win32_SetWindowLong, _win32_setwindowlong_cpp, winmsg.setwindowlong, winui._win32_setwindowlong, winuser/SetWindowLong, winuser/SetWindowLongA, winuser/SetWindowLongW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetWindowLongW (Unicode) and SetWindowLongA (ANSI)
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
 - SetWindowLongA
 - winuser/SetWindowLongA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Windowclass-l1-1-0.dll
 - Ext-MS-Win-NTUser-Windowclass-l1-1-1.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-windowclass-l1-1-2.dll
api_name:
 - SetWindowLong
 - SetWindowLongA
 - SetWindowLongW
req.apiset: ext-ms-win-ntuser-windowclass-l1-1-0 (introduced in Windows 8)
---

# SetWindowLongA function


## -description

Changes an attribute of the specified window. The function also sets the 32-bit (long) value at the specified offset into the extra window memory.
<div class="alert"><b>Note</b>  This function has been superseded by the <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlongptra">SetWindowLongPtr</a> function. To write code that is compatible with both 32-bit and 64-bit versions of Windows, use the <b>SetWindowLongPtr</b> function.</div><div> </div>

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window and, indirectly, the class to which the window belongs.

### -param nIndex [in]

Type: <b>int</b>

The zero-based offset to the value to be set. Valid values are in the range zero through the number of bytes of extra window memory, minus the size of an integer. To set any other value, specify one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GWL_EXSTYLE"></a><a id="gwl_exstyle"></a><dl>
<dt><b>GWL_EXSTYLE</b></dt>
<dt>-20</dt>
</dl>
</td>
<td width="60%">
Sets a new <a href="/windows/desktop/winmsg/extended-window-styles">extended window style</a>. 

</td>
</tr>
<tr>
<td width="40%"><a id="GWL_HINSTANCE"></a><a id="gwl_hinstance"></a><dl>
<dt><b>GWL_HINSTANCE</b></dt>
<dt>-6</dt>
</dl>
</td>
<td width="60%">
Sets a new application instance handle.

</td>
</tr>
<tr>
<td width="40%"><a id="GWL_HWNDPARENT"></a><a id="gwl_hwndparent"></a><dl>
<dt><b>GWL_HWNDPARENT</b></dt>
<dt>-8</dt>
</dl>
</td>
<td width="60%">
Sets a new owner for a top-level window.

</td>
</tr>
<tr>
<td width="40%"><a id="GWL_ID"></a><a id="gwl_id"></a><dl>
<dt><b>GWL_ID</b></dt>
<dt>-12</dt>
</dl>
</td>
<td width="60%">
Sets a new identifier of the child window. The window cannot be a top-level window.

</td>
</tr>
<tr>
<td width="40%"><a id="GWL_STYLE"></a><a id="gwl_style"></a><dl>
<dt><b>GWL_STYLE</b></dt>
<dt>-16</dt>
</dl>
</td>
<td width="60%">
Sets a new <a href="/windows/desktop/winmsg/window-styles">window style</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GWL_USERDATA"></a><a id="gwl_userdata"></a><dl>
<dt><b>GWL_USERDATA</b></dt>
<dt>-21</dt>
</dl>
</td>
<td width="60%">
Sets the user data associated with the window. This data is intended for use by the application that created the window. Its value is initially zero.

</td>
</tr>
<tr>
<td width="40%"><a id="GWL_WNDPROC"></a><a id="gwl_wndproc"></a><dl>
<dt><b>GWL_WNDPROC</b></dt>
<dt>-4</dt>
</dl>
</td>
<td width="60%">
Sets a new address for the window procedure.

You cannot change this attribute if the window does not belong to the same process as the calling thread.

</td>
</tr>
</table>
 


The following values are also available when the <i>hWnd</i> parameter identifies a dialog box.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DWL_DLGPROC"></a><a id="dwl_dlgproc"></a><dl>
<dt><b>DWL_DLGPROC</b></dt>
<dt>DWLP_MSGRESULT + sizeof(LRESULT)</dt>
</dl>
</td>
<td width="60%">
Sets the new address of the dialog box procedure.

</td>
</tr>
<tr>
<td width="40%"><a id="DWL_MSGRESULT"></a><a id="dwl_msgresult"></a><dl>
<dt><b>DWL_MSGRESULT</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Sets the return value of a message processed in the dialog box procedure.

</td>
</tr>
<tr>
<td width="40%"><a id="DWL_USER"></a><a id="dwl_user"></a><dl>
<dt><b>DWL_USER</b></dt>
<dt>DWLP_DLGPROC + sizeof(DLGPROC)</dt>
</dl>
</td>
<td width="60%">
Sets new extra information that is private to the application, such as handles or pointers.

</td>
</tr>
</table>

### -param dwNewLong [in]

Type: <b>LONG</b>

The replacement value.

## -returns

Type: <b>LONG</b>

If the function succeeds, the return value is the previous value of the specified 32-bit integer.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 

If the previous value of the specified 32-bit integer is zero, and the function succeeds, the return value is zero, but the function does not clear the last error information. This makes it difficult to determine success or failure. To deal with this, you should clear the last error information by calling <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> with 0 before calling <b>SetWindowLong</b>. Then, function failure will be indicated by a return value of zero and a <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> result that is nonzero.

## -remarks

Certain window data is cached, so changes you make using <b>SetWindowLong</b> will not take effect until you call the <a href="/windows/desktop/api/winuser/nf-winuser-setwindowpos">SetWindowPos</a> function. Specifically, if you change any of the frame styles, you must call <b>SetWindowPos</b> with the <b>SWP_FRAMECHANGED</b> flag for the cache to be updated properly. 

If you use <b>SetWindowLong</b> with the <b>GWL_WNDPROC</b> index to replace the window procedure, the window procedure must conform to the guidelines specified in the description of the <a href="/windows/win32/api/winuser/nc-winuser-wndproc">WindowProc</a> callback function. 

If you use <b>SetWindowLong</b> with the <b>DWL_MSGRESULT</b> index to set the return value for a message processed by a dialog procedure, you should return <b>TRUE</b> directly afterward. Otherwise, if you call any function that results in your dialog procedure receiving a window message, the nested window message could overwrite the return value you set using <b>DWL_MSGRESULT</b>. 

Calling <b>SetWindowLong</b> with the <b>GWL_WNDPROC</b> index creates a subclass of the window class used to create the window. An application can subclass a system class, but should not subclass a window class created by another process. The <b>SetWindowLong</b> function creates the window subclass by changing the window procedure associated with a particular window class, causing the system to call the new window procedure instead of the previous one. An application must pass any messages not processed by the new window procedure to the previous window procedure by calling <a href="/windows/desktop/api/winuser/nf-winuser-callwindowproca">CallWindowProc</a>. This allows the application to create a chain of window procedures. 

Reserve extra window memory by specifying a nonzero value in the 
				<b>cbWndExtra</b> member of the <a href="/windows/desktop/api/winuser/ns-winuser-wndclassexa">WNDCLASSEX</a> structure used with the <a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a> function. 

Do not call <b>SetWindowLong</b> with the <b>GWL_HWNDPARENT</b> index to change the parent of a child window. Instead, use the <a href="/windows/desktop/api/winuser/nf-winuser-setparent">SetParent</a> function. 

<b>GWL_HWNDPARENT</b> is used to change the owner of a top-level window, not the parent of a child window.

A window can have either a parent or an owner, or neither, but never both simultaneously.

If the window has a class style of <b>CS_CLASSDC</b> or <b>CS_OWNDC</b>, do not set the extended window styles <b>WS_EX_COMPOSITED</b> or <b>WS_EX_LAYERED</b>.

Calling <b>SetWindowLong</b> to set the style on a progressbar will reset its position.


#### Examples

For an example, see <a href="/windows/desktop/winmsg/using-window-procedures">Subclassing a Window</a>.

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines SetWindowLong as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-callwindowproca">CallWindowProc</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getwindowlonga">GetWindowLong</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setparent">SetParent</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowlongptra">SetWindowLongPtr</a>



<a href="/windows/desktop/api/winuser/ns-winuser-wndclassexa">WNDCLASSEX</a>



<a href="/windows/desktop/winmsg/window-classes">Window Classes</a>



<a href="/windows/win32/api/winuser/nc-winuser-wndproc">WindowProc</a>
