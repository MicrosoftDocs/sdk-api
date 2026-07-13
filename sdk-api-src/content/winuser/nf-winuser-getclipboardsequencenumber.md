---
UID: NF:winuser.GetClipboardSequenceNumber
title: GetClipboardSequenceNumber function (winuser.h)
description: Retrieves the clipboard sequence number for the current window station.
helpviewer_keywords: ["GetClipboardSequenceNumber","GetClipboardSequenceNumber function [Data Exchange]","_win32_GetClipboardSequenceNumber","_win32_getclipboardsequencenumber_cpp","dataxchg.getclipboardsequencenumber","winui._win32_getclipboardsequencenumber","winuser/GetClipboardSequenceNumber"]
old-location: dataxchg\getclipboardsequencenumber.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\getclipboardsequencenumber.htm
ms.date: 12/05/2018
ms.keywords: GetClipboardSequenceNumber, GetClipboardSequenceNumber function [Data Exchange], _win32_GetClipboardSequenceNumber, _win32_getclipboardsequencenumber_cpp, dataxchg.getclipboardsequencenumber, winui._win32_getclipboardsequencenumber, winuser/GetClipboardSequenceNumber
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
 - GetClipboardSequenceNumber
 - winuser/GetClipboardSequenceNumber
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
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - GetClipboardSequenceNumber
req.apiset: ext-ms-win-ntuser-misc-l1-5-1 (introduced in Windows 10, version 10.0.14393)
---

# GetClipboardSequenceNumber function


## -description

Retrieves the clipboard sequence number for the current window station.



## -returns

Type: <b>DWORD</b>

The return value is the clipboard sequence number. If you do not have <b>WINSTA_ACCESSCLIPBOARD</b> access to the window station, the function returns zero.

## -remarks

The system keeps a serial number for the clipboard for each window station. This number is incremented whenever the contents of the clipboard change or the clipboard is emptied. You can track this value to determine whether the clipboard contents have changed and optimize creating DataObjects. If clipboard rendering is delayed, the sequence number is not incremented until the changes are rendered.

## -see-also

<a href="/windows/desktop/dataxchg/clipboard">Clipboard</a>
