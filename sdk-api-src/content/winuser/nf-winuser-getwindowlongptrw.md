---
UID: NF:winuser.GetWindowLongPtrW
title: GetWindowLongPtrW function (winuser.h)
description: Retrieves information about the specified window. The function also retrieves the value at a specified offset into the extra window memory. (Unicode)
helpviewer_keywords: ["DWLP_DLGPROC", "DWLP_MSGRESULT", "DWLP_USER", "GWLP_HINSTANCE", "GWLP_HWNDPARENT", "GWLP_ID", "GWLP_USERDATA", "GWLP_WNDPROC", "GWL_EXSTYLE", "GWL_STYLE", "GetWindowLongPtr", "GetWindowLongPtr function [Windows and Messages]", "GetWindowLongPtrW", "_win32_GetWindowLongPtr", "_win32_getwindowlongptr_cpp", "winmsg.getwindowlongptr", "winui._win32_getwindowlongptr", "winuser/GetWindowLongPtr", "winuser/GetWindowLongPtrW"]
old-location: winmsg\getwindowlongptr.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowclasses\windowclassreference\windowclassfunctions\getwindowlongptr.htm
ms.date: 12/05/2018
ms.keywords: DWLP_DLGPROC, DWLP_MSGRESULT, DWLP_USER, GWLP_HINSTANCE, GWLP_HWNDPARENT, GWLP_ID, GWLP_USERDATA, GWLP_WNDPROC, GWL_EXSTYLE, GWL_STYLE, GetWindowLongPtr, GetWindowLongPtr function [Windows and Messages], GetWindowLongPtrA, GetWindowLongPtrW, _win32_GetWindowLongPtr, _win32_getwindowlongptr_cpp, winmsg.getwindowlongptr, winui._win32_getwindowlongptr, winuser/GetWindowLongPtr, winuser/GetWindowLongPtrA, winuser/GetWindowLongPtrW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetWindowLongPtrW (Unicode) and GetWindowLongPtrA (ANSI)
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
 - GetWindowLongPtrW
 - winuser/GetWindowLongPtrW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-window-l1-1-0.dll
 - ext-ms-win-rtcore-ntuser-window-ext-l1-1-1.dll
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
 - GetWindowLongPtr
 - GetWindowLongPtrA
 - GetWindowLongPtrW
req.apiset: ext-ms-win-ntuser-windowclass-l1-1-0 (introduced in Windows 8)
---

# GetWindowLongPtrW function


## -description

Retrieves information about the specified window. The function also retrieves the value at a specified offset into the extra window memory. 
<div class="alert"><b>Note</b>  To write code that is compatible with both 32-bit and 64-bit versions of Windows, use <b>GetWindowLongPtr</b>. When compiling for 32-bit Windows, <b>GetWindowLongPtr</b> is defined as a call to the <a href="/windows/desktop/api/winuser/nf-winuser-getwindowlonga">GetWindowLong</a> function.</div><div> </div>

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window and, indirectly, the class to which the window belongs.

### -param nIndex [in]

Type: <b>int</b>

The zero-based offset to the value to be retrieved. Valid values are in the range zero through the number of bytes of extra window memory, minus the size of a <b>LONG_PTR</b>. To retrieve any other value, specify one of the following values.

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
Retrieves the <a href="/windows/desktop/winmsg/extended-window-styles">extended window styles</a>. 

</td>
</tr>
<tr>
<td width="40%"><a id="GWLP_HINSTANCE"></a><a id="gwlp_hinstance"></a><dl>
<dt><b>GWLP_HINSTANCE</b></dt>
<dt>-6</dt>
</dl>
</td>
<td width="60%">
Retrieves a handle to the application instance.

</td>
</tr>
<tr>
<td width="40%"><a id="GWLP_HWNDPARENT"></a><a id="gwlp_hwndparent"></a><dl>
<dt><b>GWLP_HWNDPARENT</b></dt>
<dt>-8</dt>
</dl>
</td>
<td width="60%">
Retrieves a handle to the parent window, if there is one.

</td>
</tr>
<tr>
<td width="40%"><a id="GWLP_ID"></a><a id="gwlp_id"></a><dl>
<dt><b>GWLP_ID</b></dt>
<dt>-12</dt>
</dl>
</td>
<td width="60%">
Retrieves the identifier of the window.

</td>
</tr>
<tr>
<td width="40%"><a id="GWL_STYLE"></a><a id="gwl_style"></a><dl>
<dt><b>GWL_STYLE</b></dt>
<dt>-16</dt>
</dl>
</td>
<td width="60%">
Retrieves the <a href="/windows/desktop/winmsg/window-styles">window styles</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GWLP_USERDATA"></a><a id="gwlp_userdata"></a><dl>
<dt><b>GWLP_USERDATA</b></dt>
<dt>-21</dt>
</dl>
</td>
<td width="60%">
Retrieves the user data associated with the window. This data is intended for use by the application that created the window. Its value is initially zero.

</td>
</tr>
<tr>
<td width="40%"><a id="GWLP_WNDPROC"></a><a id="gwlp_wndproc"></a><dl>
<dt><b>GWLP_WNDPROC</b></dt>
<dt>-4</dt>
</dl>
</td>
<td width="60%">
Retrieves the pointer to the window procedure, or a handle representing the pointer to the window procedure. You must use the <a href="/windows/desktop/api/winuser/nf-winuser-callwindowproca">CallWindowProc</a> function to call the window procedure.

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
<td width="40%"><a id="DWLP_DLGPROC"></a><a id="dwlp_dlgproc"></a><dl>
<dt><b>DWLP_DLGPROC</b></dt>
<dt>DWLP_MSGRESULT + sizeof(LRESULT)</dt>
</dl>
</td>
<td width="60%">
Retrieves the pointer to the dialog box procedure, or a handle representing the pointer to the dialog box procedure. You must use the <a href="/windows/desktop/api/winuser/nf-winuser-callwindowproca">CallWindowProc</a> function to call the dialog box procedure.

</td>
</tr>
<tr>
<td width="40%"><a id="DWLP_MSGRESULT"></a><a id="dwlp_msgresult"></a><dl>
<dt><b>DWLP_MSGRESULT</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Retrieves the return value of a message processed in the dialog box procedure.

</td>
</tr>
<tr>
<td width="40%"><a id="DWLP_USER"></a><a id="dwlp_user"></a><dl>
<dt><b>DWLP_USER</b></dt>
<dt>DWLP_DLGPROC + sizeof(DLGPROC)</dt>
</dl>
</td>
<td width="60%">
Retrieves extra information private to the application, such as handles or pointers.

</td>
</tr>
</table>

## -returns

Type: <b>LONG_PTR</b>

If the function succeeds, the return value is the requested value.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 

If <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga">SetWindowLong</a> or <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlongptra">SetWindowLongPtr</a> has not been called previously, <b>GetWindowLongPtr</b> returns zero for values in the extra window or class memory.

## -remarks

Reserve extra window memory by specifying a nonzero value in the 
				<b>cbWndExtra</b> member of the <a href="/windows/desktop/api/winuser/ns-winuser-wndclassexa">WNDCLASSEX</a> structure used with the <a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a> function. 





> [!NOTE]
> The winuser.h header defines GetWindowLongPtr as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-callwindowproca">CallWindowProc</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setparent">SetParent</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowlongptra">SetWindowLongPtr</a>



<a href="/windows/desktop/api/winuser/ns-winuser-wndclassexa">WNDCLASSEX</a>



<a href="/windows/desktop/winmsg/window-classes">Window Classes</a>
