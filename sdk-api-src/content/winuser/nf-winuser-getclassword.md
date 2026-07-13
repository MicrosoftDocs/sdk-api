---
UID: NF:winuser.GetClassWord
title: GetClassWord function (winuser.h)
description: Retrieves the 16-bit (WORD) value at the specified offset into the extra class memory for the window class to which the specified window belongs.
helpviewer_keywords: ["GCW_ATOM","GetClassWord","GetClassWord function [Windows and Messages]","_win32_GetClassWord","_win32_getclassword_cpp","winmsg.getclassword","winui._win32_getclassword","winuser/GetClassWord"]
old-location: winmsg\getclassword.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowclasses\windowclassreference\windowclassfunctions\getclassword.htm
ms.date: 12/05/2018
ms.keywords: GCW_ATOM, GetClassWord, GetClassWord function [Windows and Messages], _win32_GetClassWord, _win32_getclassword_cpp, winmsg.getclassword, winui._win32_getclassword, winuser/GetClassWord
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
 - GetClassWord
 - winuser/GetClassWord
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - ext-ms-win-ntuser-windowclass-l1-1-2.dll
api_name:
 - GetClassWord
req.apiset: ext-ms-win-ntuser-windowclass-l1-1-2 (introduced in Windows 10, version 10.0.10240)
---

# GetClassWord function


## -description

Retrieves the 16-bit (<b>WORD</b>) value at the specified offset into the extra class memory for the window class to which the specified window belongs. 
		
<div class="alert"><b>Note</b>  This function is deprecated for any use other than <i>nIndex</i> set to <b>GCW_ATOM</b>. The function is provided only for compatibility with 16-bit versions of Windows. Applications should use the <a href="/windows/desktop/api/winuser/nf-winuser-getclasslonga">GetClassLong</a> or <a href="/windows/desktop/api/winuser/nf-winuser-getclasslongptra">GetClassLongPtr</a> function.</div><div> </div>

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window and, indirectly, the class to which the window belongs.

### -param nIndex [in]

Type: <b>int</b>

The zero-based byte offset of the value to be retrieved. Valid values are in the range zero through the number of bytes of class memory, minus two; for example, if you specified 10 or more bytes of extra class memory, a value of eight would be an index to the fifth 16-bit integer. There is an additional valid value as shown in the following table. 

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
Retrieves an <b>ATOM</b> value that uniquely identifies the window class. This is the same atom that the <a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a> or <a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a> function returns.

</td>
</tr>
</table>

## -returns

Type: <b>WORD</b>

If the function succeeds, the return value is the requested 16-bit value.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Reserve extra class memory by specifying a nonzero value in the 
				<b>cbClsExtra</b> member of the <a href="/windows/desktop/api/winuser/ns-winuser-wndclassa">WNDCLASS</a> structure used with the <a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a> function.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getclasslonga">GetClassLong</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a>



<a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setclassword">SetClassWord</a>



<a href="/windows/desktop/api/winuser/ns-winuser-wndclassa">WNDCLASS</a>



<a href="/windows/desktop/winmsg/window-classes">Window Classes</a>
