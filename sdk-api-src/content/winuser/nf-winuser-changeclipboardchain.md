---
UID: NF:winuser.ChangeClipboardChain
title: ChangeClipboardChain function (winuser.h)
description: Removes a specified window from the chain of clipboard viewers.
helpviewer_keywords: ["ChangeClipboardChain","ChangeClipboardChain function [Data Exchange]","_win32_ChangeClipboardChain","_win32_changeclipboardchain_cpp","dataxchg.changeclipboardchain","winui._win32_changeclipboardchain","winuser/ChangeClipboardChain"]
old-location: dataxchg\changeclipboardchain.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\changeclipboardchain.htm
ms.date: 12/05/2018
ms.keywords: ChangeClipboardChain, ChangeClipboardChain function [Data Exchange], _win32_ChangeClipboardChain, _win32_changeclipboardchain_cpp, dataxchg.changeclipboardchain, winui._win32_changeclipboardchain, winuser/ChangeClipboardChain
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
 - ChangeClipboardChain
 - winuser/ChangeClipboardChain
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - ChangeClipboardChain
req.apiset: ext-ms-win-ntuser-misc-l1-5-1 (introduced in Windows 10, version 10.0.14393)
---

# ChangeClipboardChain function


## -description

Removes a specified window from the chain of clipboard viewers.

## -parameters

### -param hWndRemove [in]

Type: <b>HWND</b>

A handle to the window to be removed from the chain. The handle must have been passed to the <a href="/windows/desktop/api/winuser/nf-winuser-setclipboardviewer">SetClipboardViewer</a> function.

### -param hWndNewNext [in]

Type: <b>HWND</b>

A handle to the window that follows the 
     <i>hWndRemove</i> window in the clipboard viewer chain. (This is the handle returned by <a href="/windows/desktop/api/winuser/nf-winuser-setclipboardviewer">SetClipboardViewer</a>, unless the sequence was changed in response to a <a href="/windows/desktop/dataxchg/wm-changecbchain">WM_CHANGECBCHAIN</a> message.)

## -returns

Type: <b>BOOL</b>

The return value indicates the result of passing the <a href="/windows/desktop/dataxchg/wm-changecbchain">WM_CHANGECBCHAIN</a> message to the windows in the clipboard viewer chain. Because a window in the chain typically returns <b>FALSE</b> when it processes <b>WM_CHANGECBCHAIN</b>, the return value from <b>ChangeClipboardChain</b> is typically <b>FALSE</b>. If there is only one window in the chain, the return value is typically <b>TRUE</b>.

## -remarks

The window identified by 
    <i>hWndNewNext</i> replaces the 
    <i>hWndRemove</i> window in the chain. The <a href="/windows/desktop/api/winuser/nf-winuser-setclipboardviewer">SetClipboardViewer</a> function sends a <a href="/windows/desktop/dataxchg/wm-changecbchain">WM_CHANGECBCHAIN</a> message to the first window in the clipboard viewer chain.

For an example, see <a href="/windows/desktop/dataxchg/using-the-clipboard">Removing a Window from the Clipboard Viewer Chain</a>.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-changeclipboardchain">ChangeClipboardChain</a>



<a href="/windows/desktop/dataxchg/clipboard">Clipboard</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setclipboardviewer">SetClipboardViewer</a>



<a href="/windows/desktop/dataxchg/wm-changecbchain">WM_CHANGECBCHAIN</a>
