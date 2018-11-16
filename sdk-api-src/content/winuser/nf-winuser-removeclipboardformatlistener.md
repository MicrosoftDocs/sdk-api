---
UID: NF:winuser.RemoveClipboardFormatListener
title: RemoveClipboardFormatListener function
author: windows-sdk-content
description: Removes the given window from the system-maintained clipboard format listener list.
old-location: dataxchg\removeclipboardformatlistener.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\removeclipboardformatlistener.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: RemoveClipboardFormatListener, RemoveClipboardFormatListener function [Data Exchange], _win32_RemoveClipboardFormatListener, _win32_removeclipboardformatlistener_cpp, dataxchg.removeclipboardformatlistener, winui._win32_removeclipboardformatlistener, winuser/RemoveClipboardFormatListener
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
- apiref
: 
- 
: 
- RemoveClipboardFormatListener
: 
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



When a window has been removed from the clipboard format listener list, it will no longer receive <a href="https://msdn.microsoft.com/1508aa22-9cf0-40a2-8cb0-ce7c8671df2c">WM_CLIPBOARDUPDATE</a> messages.




## -see-also




<a href="https://msdn.microsoft.com/0df088fd-59f4-437e-ab9a-00f0a2af332d">AddClipboardFormatListener</a>



<a href="https://msdn.microsoft.com/5790fb14-473a-49fc-943b-9cc5f1170181">GetClipboardSequenceNumber</a>



<a href="https://msdn.microsoft.com/1508aa22-9cf0-40a2-8cb0-ce7c8671df2c">WM_CLIPBOARDUPDATE</a>
 

 

