---
UID: NF:shlobj_core.IProgressDialog.SetProgress64
title: IProgressDialog::SetProgress64 (shlobj_core.h)
description: Updates the progress dialog box with the current state of the operation. (IProgressDialog.SetProgress64)
helpviewer_keywords: ["IProgressDialog interface [Windows Shell]","SetProgress64 method","IProgressDialog.SetProgress64","IProgressDialog::SetProgress64","SetProgress64","SetProgress64 method [Windows Shell]","SetProgress64 method [Windows Shell]","IProgressDialog interface","_win32_IProgressDialog_SetProgress64","shell.IProgressDialog_SetProgress64","shlobj_core/IProgressDialog::SetProgress64"]
old-location: shell\IProgressDialog_SetProgress64.htm
tech.root: shell
ms.assetid: 829775a0-5dd0-4c5e-8b92-b34c7d75f15e
ms.date: 12/05/2018
ms.keywords: IProgressDialog interface [Windows Shell],SetProgress64 method, IProgressDialog.SetProgress64, IProgressDialog::SetProgress64, SetProgress64, SetProgress64 method [Windows Shell], SetProgress64 method [Windows Shell],IProgressDialog interface, _win32_IProgressDialog_SetProgress64, shell.IProgressDialog_SetProgress64, shlobj_core/IProgressDialog::SetProgress64
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
 - IProgressDialog::SetProgress64
 - shlobj_core/IProgressDialog::SetProgress64
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
 - IProgressDialog.SetProgress64
---

# IProgressDialog::SetProgress64


## -description

Updates the progress dialog box with the current state of the operation.

## -parameters

### -param ullCompleted [in]

Type: <b>ULONGLONG</b>

An application-defined value that indicates what proportion of the operation has been completed at the time the method was called.

### -param ullTotal [in]

Type: <b>ULONGLONG</b>

An application-defined value that specifies what value <i>ullCompleted</i> will have when the operation is complete.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method has exactly the same function as <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iprogressdialog-setprogress">IProgressDialog::SetProgress</a> but allows you to use values larger than one <b>DWORD</b> (4 GB).

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iprogressdialog">IProgressDialog</a>
