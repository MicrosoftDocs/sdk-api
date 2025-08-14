---
UID: NF:winuser.CloseClipboard
title: CloseClipboard function (winuser.h)
description: Closes the clipboard.
helpviewer_keywords: ["CloseClipboard","CloseClipboard function [Data Exchange]","_win32_CloseClipboard","_win32_closeclipboard_cpp","dataxchg.closeclipboard","winui._win32_closeclipboard","winuser/CloseClipboard"]
old-location: dataxchg\closeclipboard.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\closeclipboard.htm
ms.date: 12/05/2018
ms.keywords: CloseClipboard, CloseClipboard function [Data Exchange], _win32_CloseClipboard, _win32_closeclipboard_cpp, dataxchg.closeclipboard, winui._win32_closeclipboard, winuser/CloseClipboard
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
 - CloseClipboard
 - winuser/CloseClipboard
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-misc-l1-1-0.dll
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - User32.dll
 - API-MS-Win-RTCore-NTUser-clipboard-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - api-ms-win-ntuser-ie-clipboard-l1-1-0.dll
 - ie_stubs.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - CloseClipboard
req.apiset: ext-ms-win-ntuser-misc-l1-2-0 (introduced in Windows 8.1)
---

# CloseClipboard function


## -description

Closes the clipboard.



## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

When the window has finished examining or changing the clipboard, close the clipboard by calling <b>CloseClipboard</b>. This enables other windows to access the clipboard.

Do not place an object on the clipboard after calling <b>CloseClipboard</b>. 


#### Examples

For an example, see <a href="/windows/desktop/dataxchg/using-the-clipboard">Example of a Clipboard Viewer</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/dataxchg/clipboard">Clipboard</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getopenclipboardwindow">GetOpenClipboardWindow</a>



<a href="/windows/desktop/api/winuser/nf-winuser-openclipboard">OpenClipboard</a>



<b>Reference</b>
