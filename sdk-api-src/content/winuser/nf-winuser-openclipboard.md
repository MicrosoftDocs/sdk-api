---
UID: NF:winuser.OpenClipboard
title: OpenClipboard function (winuser.h)
description: Opens the clipboard for examination and prevents other applications from modifying the clipboard content.
helpviewer_keywords: ["OpenClipboard","OpenClipboard function [Data Exchange]","_win32_OpenClipboard","_win32_openclipboard_cpp","dataxchg.openclipboard","winui._win32_openclipboard","winuser/OpenClipboard"]
old-location: dataxchg\openclipboard.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\openclipboard.htm
ms.date: 12/05/2018
ms.keywords: OpenClipboard, OpenClipboard function [Data Exchange], _win32_OpenClipboard, _win32_openclipboard_cpp, dataxchg.openclipboard, winui._win32_openclipboard, winuser/OpenClipboard
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
 - OpenClipboard
 - winuser/OpenClipboard
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
 - OpenClipboard
req.apiset: ext-ms-win-ntuser-misc-l1-2-0 (introduced in Windows 8.1)
---

# OpenClipboard function


## -description

Opens the clipboard for examination and prevents other applications from modifying the clipboard content.

## -parameters

### -param hWndNewOwner [in, optional]

Type: <b>HWND</b>

A handle to the window to be associated with the open clipboard. If this parameter is <b>NULL</b>, the open clipboard is associated with the current task.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>OpenClipboard</b> fails if another window has the clipboard open. 

An application should call the <a href="/windows/desktop/api/winuser/nf-winuser-closeclipboard">CloseClipboard</a> function after every successful call to <b>OpenClipboard</b>. 

The window identified by the 
				<i>hWndNewOwner</i> parameter does not become the clipboard owner unless the <a href="/windows/desktop/api/winuser/nf-winuser-emptyclipboard">EmptyClipboard</a> function is called. 

If an application calls <b>OpenClipboard</b> with hwnd set to <b>NULL</b>, <a href="/windows/desktop/api/winuser/nf-winuser-emptyclipboard">EmptyClipboard</a> sets the clipboard owner to <b>NULL</b>; this causes <a href="/windows/desktop/api/winuser/nf-winuser-setclipboarddata">SetClipboardData</a> to fail.


#### Examples

For an example, see <a href="/windows/desktop/dataxchg/using-the-clipboard">Copying Information to the Clipboard</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/dataxchg/clipboard">Clipboard</a>



<a href="/windows/desktop/api/winuser/nf-winuser-closeclipboard">CloseClipboard</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-emptyclipboard">EmptyClipboard</a>



<b>Reference</b>
