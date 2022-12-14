---
UID: NF:shobjidl_core.IFileDialog.GetResult
title: IFileDialog::GetResult (shobjidl_core.h)
description: Gets the choice that the user made in the dialog.
helpviewer_keywords: ["GetResult","GetResult method [Windows Shell]","GetResult method [Windows Shell]","IFileDialog interface","IFileDialog interface [Windows Shell]","GetResult method","IFileDialog.GetResult","IFileDialog::GetResult","shell.IFileDialog_GetResult","shell_IFileDialog_GetResult","shobjidl_core/IFileDialog::GetResult"]
old-location: shell\IFileDialog_GetResult.htm
tech.root: shell
ms.assetid: 6572f172-8b66-4b42-b087-d0133595b380
ms.date: 12/05/2018
ms.keywords: GetResult, GetResult method [Windows Shell], GetResult method [Windows Shell],IFileDialog interface, IFileDialog interface [Windows Shell],GetResult method, IFileDialog.GetResult, IFileDialog::GetResult, shell.IFileDialog_GetResult, shell_IFileDialog_GetResult, shobjidl_core/IFileDialog::GetResult
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
 - IFileDialog::GetResult
 - shobjidl_core/IFileDialog::GetResult
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
 - IFileDialog.GetResult
---

# IFileDialog::GetResult


## -description

Gets the choice that the user made in the dialog.

## -parameters

### -param ppsi [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>**</b>

The address of a pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that represents the user's choice.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>IFileDialog::GetResult</b> can be called after the dialog has closed or during the handling of an <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfileok">OnFileOk</a> event. Calling this method at any other time will fail. If multiple items were chosen, this method will fail. In the case of multiple items, call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults">GetResults</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show">Show</a> must return a success code for a result to be available to <b>IFileDialog::GetResult</b>.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getcurrentselection">IFileDialog::GetCurrentSelection</a>