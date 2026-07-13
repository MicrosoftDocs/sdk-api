---
UID: NF:shlobj_core.IProgressDialog.SetLine
title: IProgressDialog::SetLine (shlobj_core.h)
description: Displays a message in the progress dialog.
helpviewer_keywords: ["IProgressDialog interface [Windows Shell]","SetLine method","IProgressDialog.SetLine","IProgressDialog::SetLine","SetLine","SetLine method [Windows Shell]","SetLine method [Windows Shell]","IProgressDialog interface","_win32_IProgressDialog_SetLine","shell.IProgressDialog_SetLine","shlobj_core/IProgressDialog::SetLine"]
old-location: shell\IProgressDialog_SetLine.htm
tech.root: shell
ms.assetid: 2c4441a8-3bb6-4cd8-8f96-423ee8d26113
ms.date: 12/05/2018
ms.keywords: IProgressDialog interface [Windows Shell],SetLine method, IProgressDialog.SetLine, IProgressDialog::SetLine, SetLine, SetLine method [Windows Shell], SetLine method [Windows Shell],IProgressDialog interface, _win32_IProgressDialog_SetLine, shell.IProgressDialog_SetLine, shlobj_core/IProgressDialog::SetLine
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IProgressDialog::SetLine
 - shlobj_core/IProgressDialog::SetLine
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IProgressDialog.SetLine
---

# IProgressDialog::SetLine


## -description

Displays a message in the progress dialog.

## -parameters

### -param dwLineNum

Type: <b>DWORD</b>

The line number on which the text is to be displayed. Currently there are three lines—1, 2, and 3. If the <b>PROGDLG_AUTOTIME</b> flag was included in the <i>dwFlags</i> parameter when <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iprogressdialog-startprogressdialog">IProgressDialog::StartProgressDialog</a> was called, only lines 1 and 2 can be used. The estimated time will be displayed on line 3.

### -param pwzString [in]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that contains the text.

### -param fCompactPath

Type: <b>BOOL</b>

<b>TRUE</b> to have path strings compacted if they are too large to fit on a line. The paths are compacted with <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathcompactpatha">PathCompactPath</a>.

### -param pvResevered

Type: <b>LPCVOID</b>

Reserved. Set to <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function is typically used to display a message such as "Item XXX is now being processed." typically, messages are displayed on lines 1 and 2, with line 3 reserved for the estimated time.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iprogressdialog">IProgressDialog</a>