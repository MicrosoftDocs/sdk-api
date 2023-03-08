---
UID: NF:shlobj_core.IProgressDialog.SetProgress
title: IProgressDialog::SetProgress (shlobj_core.h)
description: Updates the progress dialog box with the current state of the operation. (IProgressDialog.SetProgress)
helpviewer_keywords: ["IProgressDialog interface [Windows Shell]","SetProgress method","IProgressDialog.SetProgress","IProgressDialog::SetProgress","SetProgress","SetProgress method [Windows Shell]","SetProgress method [Windows Shell]","IProgressDialog interface","_win32_IProgressDialog_SetProgress","shell.IProgressDialog_SetProgress","shlobj_core/IProgressDialog::SetProgress"]
old-location: shell\IProgressDialog_SetProgress.htm
tech.root: shell
ms.assetid: 50df7b32-e345-4379-809f-6870b53417b8
ms.date: 12/05/2018
ms.keywords: IProgressDialog interface [Windows Shell],SetProgress method, IProgressDialog.SetProgress, IProgressDialog::SetProgress, SetProgress, SetProgress method [Windows Shell], SetProgress method [Windows Shell],IProgressDialog interface, _win32_IProgressDialog_SetProgress, shell.IProgressDialog_SetProgress, shlobj_core/IProgressDialog::SetProgress
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
 - IProgressDialog::SetProgress
 - shlobj_core/IProgressDialog::SetProgress
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
 - IProgressDialog.SetProgress
---

# IProgressDialog::SetProgress


## -description

Updates the progress dialog box with the current state of the operation.

## -parameters

### -param dwCompleted [in]

Type: <b>DWORD</b>

An application-defined value that indicates what proportion of the operation has been completed at the time the method was called.

### -param dwTotal [in]

Type: <b>DWORD</b>

An application-defined value that specifies what value <i>dwCompleted</i> will have when the operation is complete.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Use any convenient numerical measure of the progress of the operation. To use values larger than 4 gigabytes (GB), you can instead call <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iprogressdialog-setprogress64">IProgressDialog::SetProgress64</a>.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iprogressdialog">IProgressDialog</a>
