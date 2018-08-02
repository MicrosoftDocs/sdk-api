---
UID: NF:winuser.GetClipboardSequenceNumber
title: GetClipboardSequenceNumber function
author: windows-sdk-content
description: Retrieves the clipboard sequence number for the current window station.
old-location: dataxchg\getclipboardsequencenumber.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\getclipboardsequencenumber.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetClipboardSequenceNumber, GetClipboardSequenceNumber function [Data Exchange], _win32_GetClipboardSequenceNumber, _win32_getclipboardsequencenumber_cpp, dataxchg.getclipboardsequencenumber, winui._win32_getclipboardsequencenumber, winuser/GetClipboardSequenceNumber
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
 - GetClipboardSequenceNumber
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetClipboardSequenceNumber function


## -description


Retrieves the clipboard sequence number for the current window station. 


## -parameters






## -returns



Type: <b>DWORD</b>

The return value is the clipboard sequence number. If you do not have <b>WINSTA_ACCESSCLIPBOARD</b> access to the window station, the function returns zero.




## -remarks



The system keeps a serial number for the clipboard for each window station. This number is incremented whenever the contents of the clipboard change or the clipboard is emptied. You can track this value to determine whether the clipboard contents have changed and optimize creating DataObjects. If clipboard rendering is delayed, the sequence number is not incremented until the changes are rendered. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms648709(v=VS.85).aspx">Clipboard</a>
 

 

