---
UID: NF:shobjidl_core.IFileOpenDialog.GetResults
title: IFileOpenDialog::GetResults (shobjidl_core.h)
description: Gets the user's choices in a dialog that allows multiple selection.
helpviewer_keywords: ["GetResults","GetResults method [Windows Shell]","GetResults method [Windows Shell]","IFileOpenDialog interface","IFileOpenDialog interface [Windows Shell]","GetResults method","IFileOpenDialog.GetResults","IFileOpenDialog::GetResults","shell.IFileOpenDialog_GetResults","shell_IFileOpenDialog_GetResults","shobjidl_core/IFileOpenDialog::GetResults"]
old-location: shell\IFileOpenDialog_GetResults.htm
tech.root: shell
ms.assetid: 5c710dae-4988-4f19-beb5-2ff9cd11c596
ms.date: 12/05/2018
ms.keywords: GetResults, GetResults method [Windows Shell], GetResults method [Windows Shell],IFileOpenDialog interface, IFileOpenDialog interface [Windows Shell],GetResults method, IFileOpenDialog.GetResults, IFileOpenDialog::GetResults, shell.IFileOpenDialog_GetResults, shell_IFileOpenDialog_GetResults, shobjidl_core/IFileOpenDialog::GetResults
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
 - IFileOpenDialog::GetResults
 - shobjidl_core/IFileOpenDialog::GetResults
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
 - IFileOpenDialog.GetResults
---

# IFileOpenDialog::GetResults


## -description

Gets the user's choices in a dialog that allows multiple selection.

## -parameters

### -param ppenum [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>**</b>

The address of a pointer to an <b>IShellItemArray</b> through which the items selected in the dialog can be accessed.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method can be used whether the selection consists of a single item or multiple items.

<b>IFileOpenDialog::GetResults</b> can be called after the dialog has closed or during the handling of an IFileDialogEvents::OnFileOk event. Calling this method at any other time will fail.


<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show">Show</a> must return a success code for a result to be available to <b>IFileOpenDialog::GetResults</b>.
