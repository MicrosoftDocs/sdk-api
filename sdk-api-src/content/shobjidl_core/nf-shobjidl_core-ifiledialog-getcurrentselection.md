---
UID: NF:shobjidl_core.IFileDialog.GetCurrentSelection
title: IFileDialog::GetCurrentSelection (shobjidl_core.h)
description: Gets the user's current selection in the dialog.
helpviewer_keywords: ["GetCurrentSelection","GetCurrentSelection method [Windows Shell]","GetCurrentSelection method [Windows Shell]","IFileDialog interface","IFileDialog interface [Windows Shell]","GetCurrentSelection method","IFileDialog.GetCurrentSelection","IFileDialog::GetCurrentSelection","shell.IFileDialog_GetCurrentSelection","shell_IFileDialog_GetCurrentSelection","shobjidl_core/IFileDialog::GetCurrentSelection"]
old-location: shell\IFileDialog_GetCurrentSelection.htm
tech.root: shell
ms.assetid: b3768c15-d933-43c0-8398-f8f1c16ecbf9
ms.date: 12/05/2018
ms.keywords: GetCurrentSelection, GetCurrentSelection method [Windows Shell], GetCurrentSelection method [Windows Shell],IFileDialog interface, IFileDialog interface [Windows Shell],GetCurrentSelection method, IFileDialog.GetCurrentSelection, IFileDialog::GetCurrentSelection, shell.IFileDialog_GetCurrentSelection, shell_IFileDialog_GetCurrentSelection, shobjidl_core/IFileDialog::GetCurrentSelection
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFileDialog::GetCurrentSelection
 - shobjidl_core/IFileDialog::GetCurrentSelection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileDialog.GetCurrentSelection
---

# IFileDialog::GetCurrentSelection


## -description

Gets the user's current selection in the dialog.

## -parameters

### -param ppsi [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>**</b>

The address of a pointer to the interface that represents the item currently selected in the dialog. This item can be a file or folder selected in the view window, or something that the user has entered into the dialog's edit box. The latter case may require a parsing operation (cancelable by the user) that blocks the current thread.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The calling application is responsible for releasing the retrieved <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> when it is no longer needed.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult">IFileDialog::GetResult</a>