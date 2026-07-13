---
UID: NF:winuser.SetClipboardViewer
title: SetClipboardViewer function (winuser.h)
description: Adds the specified window to the chain of clipboard viewers. Clipboard viewer windows receive a WM_DRAWCLIPBOARD message whenever the content of the clipboard changes. This function is used for backward compatibility with earlier versions of Windows.
helpviewer_keywords: ["SetClipboardViewer","SetClipboardViewer function [Data Exchange]","_win32_SetClipboardViewer","_win32_setclipboardviewer_cpp","dataxchg.setclipboardviewer","winui._win32_setclipboardviewer","winuser/SetClipboardViewer"]
old-location: dataxchg\setclipboardviewer.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\setclipboardviewer.htm
ms.date: 12/05/2018
ms.keywords: SetClipboardViewer, SetClipboardViewer function [Data Exchange], _win32_SetClipboardViewer, _win32_setclipboardviewer_cpp, dataxchg.setclipboardviewer, winui._win32_setclipboardviewer, winuser/SetClipboardViewer
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
 - SetClipboardViewer
 - winuser/SetClipboardViewer
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
 - SetClipboardViewer
req.apiset: ext-ms-win-ntuser-misc-l1-5-1 (introduced in Windows 10, version 10.0.14393)
---

# SetClipboardViewer function


## -description

Adds the specified window to the chain of clipboard viewers. Clipboard viewer windows receive a <a href="/windows/desktop/dataxchg/wm-drawclipboard">WM_DRAWCLIPBOARD</a> message whenever the content of the clipboard changes. This function is used for backward compatibility with earlier versions of Windows.

## -parameters

### -param hWndNewViewer [in]

Type: <b>HWND</b>

A handle to the window to be added to the clipboard chain.

## -returns

Type: <b>HWND</b>

If the function succeeds, the return value identifies the next window in the clipboard viewer chain. If an error occurs or there are no other windows in the clipboard viewer chain, the return value is NULL. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The windows that are part of the clipboard viewer chain, called clipboard viewer windows, must process the clipboard messages <a href="/windows/desktop/dataxchg/wm-changecbchain">WM_CHANGECBCHAIN</a> and <a href="/windows/desktop/dataxchg/wm-drawclipboard">WM_DRAWCLIPBOARD</a>. Each clipboard viewer window calls the <a href="/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a> function to pass these messages to the next window in the clipboard viewer chain.

A clipboard viewer window must eventually remove itself from the clipboard viewer chain by calling the <a href="/windows/desktop/api/winuser/nf-winuser-changeclipboardchain">ChangeClipboardChain</a> function — for example, in response to the <a href="/windows/desktop/winmsg/wm-destroy">WM_DESTROY</a> message.

The <b>SetClipboardViewer</b> function exists to provide backward compatibility with earlier versions of Windows. The clipboard viewer chain can be broken by an application that fails to handle the clipboard chain messages properly. New applications should use more robust techniques such as the clipboard sequence number or the registration of a clipboard format listener. For further details on these alternatives techniques, see <a href="/windows/desktop/dataxchg/using-the-clipboard">Monitoring Clipboard Contents</a>.


#### Examples

For an example, see <a href="/windows/desktop/dataxchg/using-the-clipboard">Adding a Window to the Clipboard Viewer Chain</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-changeclipboardchain">ChangeClipboardChain</a>



<a href="/windows/desktop/dataxchg/clipboard">Clipboard</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getclipboardviewer">GetClipboardViewer</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a>
