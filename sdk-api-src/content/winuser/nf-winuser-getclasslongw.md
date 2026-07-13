---
UID: NF:winuser.GetClassLongW
title: GetClassLongW function (winuser.h)
description: Retrieves the specified 32-bit (DWORD) value from the WNDCLASSEX structure associated with the specified window. (Unicode)
helpviewer_keywords: ["GCL_CBCLSEXTRA", "GCL_CBWNDEXTRA", "GCL_HBRBACKGROUND", "GCL_HCURSOR", "GCL_HICON", "GCL_HICONSM", "GCL_HMODULE", "GCL_MENUNAME", "GCL_STYLE", "GCL_WNDPROC", "GCW_ATOM", "GetClassLong", "GetClassLong function [Windows and Messages]", "GetClassLongW", "_win32_GetClassLong", "_win32_getclasslong_cpp", "winmsg.getclasslong", "winui._win32_getclasslong", "winuser/GetClassLong", "winuser/GetClassLongW"]
old-location: winmsg\getclasslong.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowclasses\windowclassreference\windowclassfunctions\getclasslong.htm
ms.date: 12/05/2018
ms.keywords: GCL_CBCLSEXTRA, GCL_CBWNDEXTRA, GCL_HBRBACKGROUND, GCL_HCURSOR, GCL_HICON, GCL_HICONSM, GCL_HMODULE, GCL_MENUNAME, GCL_STYLE, GCL_WNDPROC, GCW_ATOM, GetClassLong, GetClassLong function [Windows and Messages], GetClassLongA, GetClassLongW, _win32_GetClassLong, _win32_getclasslong_cpp, winmsg.getclasslong, winui._win32_getclasslong, winuser/GetClassLong, winuser/GetClassLongA, winuser/GetClassLongW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetClassLongW (Unicode) and GetClassLongA (ANSI)
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
 - GetClassLongW
 - winuser/GetClassLongW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Windowclass-l1-1-1.dll
 - ext-ms-win-ntuser-windowclass-l1-1-2.dll
api_name:
 - GetClassLong
 - GetClassLongA
 - GetClassLongW
req.apiset: ext-ms-win-ntuser-windowclass-l1-1-1 (introduced in Windows 8.1)
---

# GetClassLongW function


## -description

Retrieves the specified 32-bit (<b>DWORD</b>) value from the <a href="/windows/desktop/api/winuser/ns-winuser-wndclassexa">WNDCLASSEX</a> structure associated with the specified window.
<div class="alert"><b>Note</b>  If you are retrieving a pointer or a handle, this function has been superseded by the <a href="/windows/desktop/api/winuser/nf-winuser-getclasslongptra">GetClassLongPtr</a> function. (Pointers and handles are 32 bits on 32-bit Windows and 64 bits on 64-bit Windows.)</div><div> </div>

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window and, indirectly, the class to which the window belongs.

### -param nIndex [in]

Type: <b>int</b>

The value to be retrieved. To retrieve a value from the extra class memory, specify the positive, zero-based byte offset of the value to be retrieved. Valid values are in the range zero through the number of bytes of extra class memory, minus four; for example, if you specified 12 or more bytes of extra class memory, a value of 8 would be an index to the third integer. To retrieve any other value from the <a href="/windows/desktop/api/winuser/ns-winuser-wndclassexa">WNDCLASSEX</a> structure, specify one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GCW_ATOM"></a><a id="gcw_atom"></a><dl>
<dt><b>GCW_ATOM</b></dt>
<dt>-32</dt>
</dl>
</td>
<td width="60%">
Retrieves an 
						<b>ATOM</b> value that uniquely identifies the window class. This is the same atom that the <a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a> function returns.

</td>
</tr>
<tr>
<td width="40%"><a id="GCL_CBCLSEXTRA"></a><a id="gcl_cbclsextra"></a><dl>
<dt><b>GCL_CBCLSEXTRA</b></dt>
<dt>-20</dt>
</dl>
</td>
<td width="60%">
Retrieves the size, in bytes, of the extra memory associated with the class.

</td>
</tr>
<tr>
<td width="40%"><a id="GCL_CBWNDEXTRA"></a><a id="gcl_cbwndextra"></a><dl>
<dt><b>GCL_CBWNDEXTRA</b></dt>
<dt>-18</dt>
</dl>
</td>
<td width="60%">
Retrieves the size, in bytes, of the extra window memory associated with each window in the class. For information on how to access this memory, see <a href="/windows/desktop/api/winuser/nf-winuser-getwindowlonga">GetWindowLong</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GCL_HBRBACKGROUND"></a><a id="gcl_hbrbackground"></a><dl>
<dt><b>GCL_HBRBACKGROUND</b></dt>
<dt>-10</dt>
</dl>
</td>
<td width="60%">
Retrieves a handle to the background brush associated with the class.

</td>
</tr>
<tr>
<td width="40%"><a id="GCL_HCURSOR"></a><a id="gcl_hcursor"></a><dl>
<dt><b>GCL_HCURSOR</b></dt>
<dt>-12</dt>
</dl>
</td>
<td width="60%">
Retrieves a handle to the cursor associated with the class.

</td>
</tr>
<tr>
<td width="40%"><a id="GCL_HICON"></a><a id="gcl_hicon"></a><dl>
<dt><b>GCL_HICON</b></dt>
<dt>-14</dt>
</dl>
</td>
<td width="60%">
Retrieves a handle to the icon associated with the class.

</td>
</tr>
<tr>
<td width="40%"><a id="GCL_HICONSM"></a><a id="gcl_hiconsm"></a><dl>
<dt><b>GCL_HICONSM</b></dt>
<dt>-34</dt>
</dl>
</td>
<td width="60%">
Retrieves a handle to the small icon associated with the class.

</td>
</tr>
<tr>
<td width="40%"><a id="GCL_HMODULE"></a><a id="gcl_hmodule"></a><dl>
<dt><b>GCL_HMODULE</b></dt>
<dt>-16</dt>
</dl>
</td>
<td width="60%">
Retrieves a handle to the module that registered the class.

</td>
</tr>
<tr>
<td width="40%"><a id="GCL_MENUNAME"></a><a id="gcl_menuname"></a><dl>
<dt><b>GCL_MENUNAME</b></dt>
<dt>-8</dt>
</dl>
</td>
<td width="60%">
Retrieves the address of the menu name string. The string identifies the menu resource associated with the class.

</td>
</tr>
<tr>
<td width="40%"><a id="GCL_STYLE"></a><a id="gcl_style"></a><dl>
<dt><b>GCL_STYLE</b></dt>
<dt>-26</dt>
</dl>
</td>
<td width="60%">
Retrieves the window-class style bits.

</td>
</tr>
<tr>
<td width="40%"><a id="GCL_WNDPROC"></a><a id="gcl_wndproc"></a><dl>
<dt><b>GCL_WNDPROC</b></dt>
<dt>-24</dt>
</dl>
</td>
<td width="60%">
Retrieves the address of the window procedure, or a handle representing the address of the window procedure. You must use the <a href="/windows/desktop/api/winuser/nf-winuser-callwindowproca">CallWindowProc</a> function to call the window procedure. 

</td>
</tr>
</table>

## -returns

Type: <b>DWORD</b>

If the function succeeds, the return value is the requested value.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Reserve extra class memory by specifying a nonzero value in the 
				<b>cbClsExtra</b> member of the <a href="/windows/desktop/api/winuser/ns-winuser-wndclassexa">WNDCLASSEX</a> structure used with the <a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a> function. 





> [!NOTE]
> The winuser.h header defines GetClassLong as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getclasslongptra">GetClassLongPtr</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getwindowlonga">GetWindowLong</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setclasslonga">SetClassLong</a>



<a href="/windows/desktop/api/winuser/ns-winuser-wndclassexa">WNDCLASSEX</a>



<a href="/windows/desktop/winmsg/window-classes">Window Classes</a>
