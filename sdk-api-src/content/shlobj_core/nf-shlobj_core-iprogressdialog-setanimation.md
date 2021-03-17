---
UID: NF:shlobj_core.IProgressDialog.SetAnimation
title: IProgressDialog::SetAnimation (shlobj_core.h)
description: Specifies an Audio-Video Interleaved (AVI) clip that runs in the dialog box.
helpviewer_keywords: ["IProgressDialog interface [Windows Shell]","SetAnimation method","IProgressDialog.SetAnimation","IProgressDialog::SetAnimation","SetAnimation","SetAnimation method [Windows Shell]","SetAnimation method [Windows Shell]","IProgressDialog interface","_win32_IProgressDialog_SetAnimation","shell.IProgressDialog_SetAnimation","shlobj_core/IProgressDialog::SetAnimation"]
old-location: shell\IProgressDialog_SetAnimation.htm
tech.root: shell
ms.assetid: cc974be9-e9a4-42f9-9995-0d6eb0b12422
ms.date: 12/05/2018
ms.keywords: IProgressDialog interface [Windows Shell],SetAnimation method, IProgressDialog.SetAnimation, IProgressDialog::SetAnimation, SetAnimation, SetAnimation method [Windows Shell], SetAnimation method [Windows Shell],IProgressDialog interface, _win32_IProgressDialog_SetAnimation, shell.IProgressDialog_SetAnimation, shlobj_core/IProgressDialog::SetAnimation
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
 - IProgressDialog::SetAnimation
 - shlobj_core/IProgressDialog::SetAnimation
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
 - IProgressDialog.SetAnimation
---

# IProgressDialog::SetAnimation


## -description

<p class="CCE_Message">[This method is not supported in Windows Vista or later versions.]

Specifies an Audio-Video Interleaved (AVI) clip that runs in the dialog box.

## -parameters

### -param hInstAnimation [in, optional]

Type: <b>HINSTANCE</b>

An instance handle to the module from which the AVI resource should be loaded.

### -param idAnimation

Type: <b>UINT</b>

An AVI resource identifier. To create this value, use the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro. The control loads the AVI resource from the module specified by <i>hInstAnimation</i>.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful, or an error value otherwise. In Windows Vista and later versions, always returns <b>S_OK</b>.

## -remarks

<b>IProgressDialog::SetAnimation</b> cannot be called before the progress dialog is visible. Until it is displayed, the progress dialog does not have a valid HWND. The existence of that HWND can be used to determine whether <b>IProgressDialog::SetAnimation</b> can be called.

This method takes the instance handle specified by <i>hInstAnimation</i> and uses an <a href="/windows/desktop/Controls/animation-control-overview">animation control</a> to open and run a silent AVI clip. There are several restrictions as to what types of AVI clips can be used, including the following:

				

<ul>
<li>Clips cannot include sound.</li>
<li>The size of the AVI clip cannot exceed 272 by 60 pixels. Smaller rectangles can be used, but they might not be properly centered.</li>
<li>AVI clips must either be uncompressed or compressed with run-length (BI_RLE8) encoding. If you attempt to use an unsupported compression type, no animation is displayed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iprogressdialog">IProgressDialog</a>
