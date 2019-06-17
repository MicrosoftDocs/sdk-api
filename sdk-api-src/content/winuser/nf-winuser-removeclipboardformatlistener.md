---
UID: NF:winuser.RemoveClipboardFormatListener
title: RemoveClipboardFormatListener function (winuser.h)
author: windows-sdk-content
description: Removes the given window from the system-maintained clipboard format listener list.
old-location: dataxchg\removeclipboardformatlistener.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\removeclipboardformatlistener.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RemoveClipboardFormatListener, RemoveClipboardFormatListener function [Data Exchange], _win32_RemoveClipboardFormatListener, _win32_removeclipboardformatlistener_cpp, dataxchg.removeclipboardformatlistener, winui._win32_removeclipboardformatlistener, winuser/RemoveClipboardFormatListener
ms.topic: function
f1_keywords: ["winuser/RemoveClipboardFormatListener"]
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - RemoveClipboardFormatListener
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RemoveClipboardFormatListener function


## -description


Removes the given window from the system-maintained clipboard format listener list.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

A handle to the window to remove from the clipboard format listener list.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful, <b>FALSE</b> otherwise. Call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> for additional details.




## -remarks



When a window has been removed from the clipboard format listener list, it will no longer receive <a href="https://docs.microsoft.com/windows/desktop/dataxchg/wm-clipboardupdate">WM_CLIPBOARDUPDATE</a> messages.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-addclipboardformatlistener">AddClipboardFormatListener</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getclipboardsequencenumber">GetClipboardSequenceNumber</a>



<a href="https://docs.microsoft.com/windows/desktop/dataxchg/wm-clipboardupdate">WM_CLIPBOARDUPDATE</a>
 

 

