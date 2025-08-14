---
UID: NF:winuser.GetClipboardViewer
title: GetClipboardViewer function (winuser.h)
description: Retrieves the handle to the first window in the clipboard viewer chain.
helpviewer_keywords: ["GetClipboardViewer","GetClipboardViewer function [Data Exchange]","_win32_GetClipboardViewer","_win32_getclipboardviewer_cpp","dataxchg.getclipboardviewer","winui._win32_getclipboardviewer","winuser/GetClipboardViewer"]
old-location: dataxchg\getclipboardviewer.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\getclipboardviewer.htm
ms.date: 12/05/2018
ms.keywords: GetClipboardViewer, GetClipboardViewer function [Data Exchange], _win32_GetClipboardViewer, _win32_getclipboardviewer_cpp, dataxchg.getclipboardviewer, winui._win32_getclipboardviewer, winuser/GetClipboardViewer
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
 - GetClipboardViewer
 - winuser/GetClipboardViewer
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
 - GetClipboardViewer
req.apiset: ext-ms-win-ntuser-misc-l1-5-1 (introduced in Windows 10, version 10.0.14393)
---

# GetClipboardViewer function


## -description

Retrieves the handle to the first window in the clipboard viewer chain.



## -returns

Type: <b>HWND</b>

If the function succeeds, the return value is the handle to the first window in the clipboard viewer chain. 

If there is no clipboard viewer, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/dataxchg/clipboard">Clipboard</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getclipboardowner">GetClipboardOwner</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setclipboardviewer">SetClipboardViewer</a>
