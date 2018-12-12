---
UID: NF:winuser.AddClipboardFormatListener
title: AddClipboardFormatListener function
author: windows-sdk-content
description: Places the given window in the system-maintained clipboard format listener list.
old-location: dataxchg\addclipboardformatlistener.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\addclipboardformatlistener.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddClipboardFormatListener, AddClipboardFormatListener function [Data Exchange], _win32_AddClipboardFormatListener, _win32_addclipboardformatlistener_cpp, dataxchg.addclipboardformatlistener, winui._win32_addclipboardformatlistener, winuser/AddClipboardFormatListener
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
 - AddClipboardFormatListener
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AddClipboardFormatListener function


## -description


Places the given window in the system-maintained clipboard format listener list.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

A handle to the window to be placed in the clipboard format listener list.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful, <b>FALSE</b> otherwise. Call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> for additional details.




## -remarks



When a window has been added to the clipboard format listener list, it is posted a <a href="https://msdn.microsoft.com/1508aa22-9cf0-40a2-8cb0-ce7c8671df2c">WM_CLIPBOARDUPDATE</a> message whenever the contents of the clipboard have changed.




## -see-also




<a href="https://msdn.microsoft.com/5790fb14-473a-49fc-943b-9cc5f1170181">GetClipboardSequenceNumber</a>



<a href="https://msdn.microsoft.com/64b18bad-ebac-4e51-9806-aa288abfc112">RemoveClipboardFormatListener</a>



<a href="https://msdn.microsoft.com/1508aa22-9cf0-40a2-8cb0-ce7c8671df2c">WM_CLIPBOARDUPDATE</a>
 

 

