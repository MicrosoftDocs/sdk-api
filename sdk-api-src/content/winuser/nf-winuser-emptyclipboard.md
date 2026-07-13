---
UID: NF:winuser.EmptyClipboard
title: EmptyClipboard function (winuser.h)
description: Empties the clipboard and frees handles to data in the clipboard. The function then assigns ownership of the clipboard to the window that currently has the clipboard open.
helpviewer_keywords: ["EmptyClipboard","EmptyClipboard function [Data Exchange]","_win32_EmptyClipboard","_win32_emptyclipboard_cpp","dataxchg.emptyclipboard","winui._win32_emptyclipboard","winuser/EmptyClipboard"]
old-location: dataxchg\emptyclipboard.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\emptyclipboard.htm
ms.date: 12/05/2018
ms.keywords: EmptyClipboard, EmptyClipboard function [Data Exchange], _win32_EmptyClipboard, _win32_emptyclipboard_cpp, dataxchg.emptyclipboard, winui._win32_emptyclipboard, winuser/EmptyClipboard
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
 - EmptyClipboard
 - winuser/EmptyClipboard
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
 - EmptyClipboard
req.apiset: ext-ms-win-ntuser-misc-l1-2-0 (introduced in Windows 8.1)
---

# EmptyClipboard function


## -description

Empties the clipboard and frees handles to data in the clipboard. The function then assigns ownership of the clipboard to the window that currently has the clipboard open.



## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Before calling <b>EmptyClipboard</b>, an application must open the clipboard by using the <a href="/windows/desktop/api/winuser/nf-winuser-openclipboard">OpenClipboard</a> function. If the application specifies a <b>NULL</b> window handle when opening the clipboard, <b>EmptyClipboard</b> succeeds but sets the clipboard owner to <b>NULL</b>. Note that this causes <a href="/windows/desktop/api/winuser/nf-winuser-setclipboarddata">SetClipboardData</a> to fail. 


#### Examples

For an example, see <a href="/windows/desktop/dataxchg/using-the-clipboard">Copying Information to the Clipboard</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/dataxchg/clipboard">Clipboard</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-openclipboard">OpenClipboard</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setclipboarddata">SetClipboardData</a>



<a href="/windows/desktop/dataxchg/wm-destroyclipboard">WM_DESTROYCLIPBOARD</a>
