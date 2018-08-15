---
UID: NF:winuser.RemoveClipboardFormatListener
title: RemoveClipboardFormatListener function
author: windows-sdk-content
description: Removes the given window from the system-maintained clipboard format listener list.
old-location: dataxchg\removeclipboardformatlistener.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\removeclipboardformatlistener.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RemoveClipboardFormatListener, RemoveClipboardFormatListener function [Data Exchange], _win32_RemoveClipboardFormatListener, _win32_removeclipboardformatlistener_cpp, dataxchg.removeclipboardformatlistener, winui._win32_removeclipboardformatlistener, winuser/RemoveClipboardFormatListener
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: 
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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

Returns <b>TRUE</b> if successful, <b>FALSE</b> otherwise. Call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> for additional details.




## -remarks



When a window has been removed from the clipboard format listener list, it will no longer receive <a href="https://msdn.microsoft.com/en-us/library/ms649021(v=VS.85).aspx">WM_CLIPBOARDUPDATE</a> messages.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms649033(v=VS.85).aspx">AddClipboardFormatListener</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649042(v=VS.85).aspx">GetClipboardSequenceNumber</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649021(v=VS.85).aspx">WM_CLIPBOARDUPDATE</a>
 

 

