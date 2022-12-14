---
UID: NF:winuser.GetCaretPos
title: GetCaretPos function (winuser.h)
description: Copies the caret's position to the specified POINT structure.
helpviewer_keywords: ["GetCaretPos","GetCaretPos function [Menus and Other Resources]","_win32_GetCaretPos","_win32_getcaretpos_cpp","menurc.getcaretpos","winui._win32_getcaretpos","winuser/GetCaretPos"]
old-location: menurc\getcaretpos.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\carets\caretreference\caretfunctions\getcaretpos.htm
ms.date: 12/05/2018
ms.keywords: GetCaretPos, GetCaretPos function [Menus and Other Resources], _win32_GetCaretPos, _win32_getcaretpos_cpp, menurc.getcaretpos, winui._win32_getcaretpos, winuser/GetCaretPos
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
 - GetCaretPos
 - winuser/GetCaretPos
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-caret-l1-1-0.dll
 - api-ms-win-ntuser-ie-caret-l1-1-0.dll
 - ie_stubs.dll
api_name:
 - GetCaretPos
req.apiset: ext-ms-win-ntuser-caret-l1-1-0 (introduced in Windows 8)
---

# GetCaretPos function


## -description

Copies the caret's position to the specified <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure.

## -parameters

### -param lpPoint [out]

Type: <b>LPPOINT</b>

A pointer to the <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that is to receive the client coordinates of the caret.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.
                

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The caret position is always given in the client coordinates of the window that contains the caret. 

<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. The returned values are interpreted as logical sizes in terms of the window in question. The calling thread is not taken into consideration.

## -see-also

<a href="/windows/desktop/menurc/carets">Carets</a>



<b>Conceptual</b>



<b>Other Resources</b>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setcaretpos">SetCaretPos</a>
