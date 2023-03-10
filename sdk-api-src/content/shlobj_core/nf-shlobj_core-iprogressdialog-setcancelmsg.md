---
UID: NF:shlobj_core.IProgressDialog.SetCancelMsg
title: IProgressDialog::SetCancelMsg (shlobj_core.h)
description: Sets a message to be displayed if the user cancels the operation.
helpviewer_keywords: ["IProgressDialog interface [Windows Shell]","SetCancelMsg method","IProgressDialog.SetCancelMsg","IProgressDialog::SetCancelMsg","SetCancelMsg","SetCancelMsg method [Windows Shell]","SetCancelMsg method [Windows Shell]","IProgressDialog interface","_win32_IProgressDialog_SetCancelMsg","shell.IProgressDialog_SetCancelMsg","shlobj_core/IProgressDialog::SetCancelMsg"]
old-location: shell\IProgressDialog_SetCancelMsg.htm
tech.root: shell
ms.assetid: 520e11c0-f356-45e1-a300-cc14e88eb42e
ms.date: 12/05/2018
ms.keywords: IProgressDialog interface [Windows Shell],SetCancelMsg method, IProgressDialog.SetCancelMsg, IProgressDialog::SetCancelMsg, SetCancelMsg, SetCancelMsg method [Windows Shell], SetCancelMsg method [Windows Shell],IProgressDialog interface, _win32_IProgressDialog_SetCancelMsg, shell.IProgressDialog_SetCancelMsg, shlobj_core/IProgressDialog::SetCancelMsg
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
 - IProgressDialog::SetCancelMsg
 - shlobj_core/IProgressDialog::SetCancelMsg
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
 - IProgressDialog.SetCancelMsg
---

# IProgressDialog::SetCancelMsg


## -description

Sets a message to be displayed if the user cancels the operation.

## -parameters

### -param pwzCancelMsg [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated Unicode string that contains the message to be displayed.

### -param pvResevered

Type: <b>LPCVOID</b>

Reserved. Set to <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Even though the user clicks <b>Cancel</b>, the application cannot immediately call <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iprogressdialog-stopprogressdialog">IProgressDialog::StopProgressDialog</a> to close the dialog box. The application must wait until the next time it calls <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iprogressdialog-hasusercancelled">IProgressDialog::HasUserCancelled</a> to discover that the user has canceled the operation. Since this delay might be significant, the progress dialog box provides the user with immediate feedback by clearing text lines 1 and 2 and displaying the cancel message on line 3. The message is intended to let the user know that the delay is normal and that the progress dialog box will be closed shortly. It is typically is set to something like "Please wait while ...".

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iprogressdialog">IProgressDialog</a>