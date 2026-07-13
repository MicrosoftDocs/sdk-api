---
UID: NF:shlobj_core.IProgressDialog.HasUserCancelled
title: IProgressDialog::HasUserCancelled (shlobj_core.h)
description: Checks whether the user has canceled the operation.
helpviewer_keywords: ["HasUserCancelled","HasUserCancelled method [Windows Shell]","HasUserCancelled method [Windows Shell]","IProgressDialog interface","IProgressDialog interface [Windows Shell]","HasUserCancelled method","IProgressDialog.HasUserCancelled","IProgressDialog::HasUserCancelled","_win32_IProgressDialog_HasUserCancelled","shell.IProgressDialog_HasUserCancelled","shlobj_core/IProgressDialog::HasUserCancelled"]
old-location: shell\IProgressDialog_HasUserCancelled.htm
tech.root: shell
ms.assetid: bd817850-7776-47cd-b1b3-ccb946660781
ms.date: 12/05/2018
ms.keywords: HasUserCancelled, HasUserCancelled method [Windows Shell], HasUserCancelled method [Windows Shell],IProgressDialog interface, IProgressDialog interface [Windows Shell],HasUserCancelled method, IProgressDialog.HasUserCancelled, IProgressDialog::HasUserCancelled, _win32_IProgressDialog_HasUserCancelled, shell.IProgressDialog_HasUserCancelled, shlobj_core/IProgressDialog::HasUserCancelled
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
 - IProgressDialog::HasUserCancelled
 - shlobj_core/IProgressDialog::HasUserCancelled
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
 - IProgressDialog.HasUserCancelled
---

# IProgressDialog::HasUserCancelled


## -description

Checks whether the user has canceled the operation.



## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if the user has canceled the operation; otherwise, <b>FALSE</b>.

## -remarks

The system does not send a message to the application when the user clicks the <b>Cancel</b> button. You must periodically use this function to poll the progress dialog box object to determine whether the operation has been canceled.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iprogressdialog">IProgressDialog</a>
