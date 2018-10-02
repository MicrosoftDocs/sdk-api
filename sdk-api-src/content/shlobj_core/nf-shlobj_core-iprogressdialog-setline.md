---
UID: NF:shlobj_core.IProgressDialog.SetLine
title: IProgressDialog::SetLine
author: windows-sdk-content
description: Displays a message in the progress dialog.
old-location: shell\IProgressDialog_SetLine.htm
tech.root: Shell
ms.assetid: 2c4441a8-3bb6-4cd8-8f96-423ee8d26113
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IProgressDialog interface [Windows Shell],SetLine method, IProgressDialog.SetLine, IProgressDialog::SetLine, SetLine, SetLine method [Windows Shell], SetLine method [Windows Shell],IProgressDialog interface, _win32_IProgressDialog_SetLine, shell.IProgressDialog_SetLine, shlobj_core/IProgressDialog::SetLine
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IProgressDialog.SetLine
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IProgressDialog::SetLine


## -description


Displays a message in the progress dialog.


## -parameters




### -param dwLineNum

Type: <b>DWORD</b>

The line number on which the text is to be displayed. Currently there are three lines—1, 2, and 3. If the <b>PROGDLG_AUTOTIME</b> flag was included in the <i>dwFlags</i> parameter when <a href="https://msdn.microsoft.com/0cafe878-c95f-416e-8291-51d9a5a17a71">IProgressDialog::StartProgressDialog</a> was called, only lines 1 and 2 can be used. The estimated time will be displayed on line 3.


### -param pwzString [in]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that contains the text.


### -param fCompactPath

Type: <b>BOOL</b>

<b>TRUE</b> to have path strings compacted if they are too large to fit on a line. The paths are compacted with <a href="https://msdn.microsoft.com/b8184c98-1f86-4714-baf8-af4ef3e71cf2">PathCompactPath</a>.


### -param pvResevered

TBD




#### - pvReserved

Type: <b>LPCVOID</b>

Reserved. Set to <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function is typically used to display a message such as "Item XXX is now being processed." typically, messages are displayed on lines 1 and 2, with line 3 reserved for the estimated time.




## -see-also




<a href="https://msdn.microsoft.com/ba0fb1f9-f67f-4cc7-96d8-4c4ccdd213eb">IProgressDialog</a>
 

 

