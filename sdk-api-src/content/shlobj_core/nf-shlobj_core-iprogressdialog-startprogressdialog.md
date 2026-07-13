---
UID: NF:shlobj_core.IProgressDialog.StartProgressDialog
title: IProgressDialog::StartProgressDialog (shlobj_core.h)
description: Starts the progress dialog box.
helpviewer_keywords: ["IProgressDialog interface [Windows Shell]","StartProgressDialog method","IProgressDialog.StartProgressDialog","IProgressDialog::StartProgressDialog","PROGDLG_AUTOTIME","PROGDLG_MARQUEEPROGRESS","PROGDLG_MODAL","PROGDLG_NOCANCEL","PROGDLG_NOMINIMIZE","PROGDLG_NOPROGRESSBAR","PROGDLG_NORMAL","PROGDLG_NOTIME","StartProgressDialog","StartProgressDialog method [Windows Shell]","StartProgressDialog method [Windows Shell]","IProgressDialog interface","_win32_IProgressDialog_StartProgressDialog","shell.IProgressDialog_StartProgressDialog","shlobj_core/IProgressDialog::StartProgressDialog"]
old-location: shell\IProgressDialog_StartProgressDialog.htm
tech.root: shell
ms.assetid: 0cafe878-c95f-416e-8291-51d9a5a17a71
ms.date: 12/05/2018
ms.keywords: IProgressDialog interface [Windows Shell],StartProgressDialog method, IProgressDialog.StartProgressDialog, IProgressDialog::StartProgressDialog, PROGDLG_AUTOTIME, PROGDLG_MARQUEEPROGRESS, PROGDLG_MODAL, PROGDLG_NOCANCEL, PROGDLG_NOMINIMIZE, PROGDLG_NOPROGRESSBAR, PROGDLG_NORMAL, PROGDLG_NOTIME, StartProgressDialog, StartProgressDialog method [Windows Shell], StartProgressDialog method [Windows Shell],IProgressDialog interface, _win32_IProgressDialog_StartProgressDialog, shell.IProgressDialog_StartProgressDialog, shlobj_core/IProgressDialog::StartProgressDialog
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
 - IProgressDialog::StartProgressDialog
 - shlobj_core/IProgressDialog::StartProgressDialog
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
 - IProgressDialog.StartProgressDialog
---

# IProgressDialog::StartProgressDialog


## -description

Starts the progress dialog box.

## -parameters

### -param hwndParent [in]

Type: <b>HWND</b>

A handle to the dialog box's parent window.

### -param punkEnableModless

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

Reserved. Set to <b>NULL</b>.

### -param dwFlags

Type: <b>DWORD</b>

Flags that control the operation of the progress dialog box. A combination of the following values:



#### PROGDLG_NORMAL

Normal progress dialog box behavior.



#### PROGDLG_MODAL

The progress dialog box will be modal to the window specified by <i>hwndParent</i>. By default, a progress dialog box is modeless.



#### PROGDLG_AUTOTIME

Automatically estimate the remaining time and display the estimate on line 3. If this flag is set, <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iprogressdialog-setline">IProgressDialog::SetLine</a> can be used only to display text on lines 1 and 2.



#### PROGDLG_NOTIME

Do not show the "time remaining" text.



#### PROGDLG_NOMINIMIZE

Do not display a minimize button on the dialog box's caption bar.



#### PROGDLG_NOPROGRESSBAR

Do not display a progress bar. Typically, an application can quantitatively determine how much of the operation remains and periodically pass that value to <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iprogressdialog-setprogress">IProgressDialog::SetProgress</a>. The progress dialog box uses this information to update its progress bar. This flag is typically set when the calling application must wait for an operation to finish, but does not have any quantitative information it can use to update the dialog box.



#### PROGDLG_MARQUEEPROGRESS

<b>Windows Vista and later.</b> Sets the progress bar to marquee mode. This causes the progress bar to scroll horizontally, similar to a marquee display. Use this when you wish to indicate that progress is being made, but the time required for the operation is unknown.



#### PROGDLG_NOCANCEL

<b>Windows Vista and later.</b> Do not display a cancel button. The operation cannot be canceled. Use this only when absolutely necessary.

### -param pvResevered

Type: <b>LPCVOID</b>

Reserved. Set to <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iprogressdialog">IProgressDialog</a>