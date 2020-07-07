---
UID: NF:winuser.GetClipboardOwner
title: GetClipboardOwner function (winuser.h)
description: Retrieves the window handle of the current owner of the clipboard.
helpviewer_keywords: ["GetClipboardOwner","GetClipboardOwner function [Data Exchange]","_win32_GetClipboardOwner","_win32_getclipboardowner_cpp","dataxchg.getclipboardowner","winui._win32_getclipboardowner","winuser/GetClipboardOwner"]
old-location: dataxchg\getclipboardowner.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\getclipboardowner.htm
ms.date: 12/05/2018
ms.keywords: GetClipboardOwner, GetClipboardOwner function [Data Exchange], _win32_GetClipboardOwner, _win32_getclipboardowner_cpp, dataxchg.getclipboardowner, winui._win32_getclipboardowner, winuser/GetClipboardOwner
f1_keywords:
- winuser/GetClipboardOwner
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- User32.dll
- Ext-MS-Win-NTUser-Misc-l1-2-0.dll
- Ext-MS-Win-NTUser-Misc-l1-3-0.dll
- ext-ms-win-ntuser-misc-l1-3-1.dll
- Ext-MS-Win-NTUser-Misc-L1-4-0.dll
- Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
- Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
- GetClipboardOwner
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetClipboardOwner function


## -description


Retrieves the window handle of the current owner of the clipboard. 


## -parameters






## -returns



Type: <b>HWND</b>

If the function succeeds, the return value is the handle to the window that owns the clipboard. 

If the clipboard is not owned, the return value is <b>NULL</b>. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 




## -remarks



The clipboard can still contain data even if the clipboard is not currently owned. 

In general, the clipboard owner is the window that last placed data in clipboard. The <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-emptyclipboard">EmptyClipboard</a> function assigns clipboard ownership. 


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/dataxchg/using-the-clipboard">Example of a Clipboard Viewer</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dataxchg/clipboard">Clipboard</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-emptyclipboard">EmptyClipboard</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getclipboardviewer">GetClipboardViewer</a>



<b>Reference</b>
 

 

