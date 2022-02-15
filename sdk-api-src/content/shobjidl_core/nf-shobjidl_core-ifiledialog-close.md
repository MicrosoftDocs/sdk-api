---
UID: NF:shobjidl_core.IFileDialog.Close
title: IFileDialog::Close (shobjidl_core.h)
description: Closes the dialog.
helpviewer_keywords: ["Close","Close method [Windows Shell]","Close method [Windows Shell]","IFileDialog interface","IFileDialog interface [Windows Shell]","Close method","IFileDialog.Close","IFileDialog::Close","shell.IFileDialog_Close","shell_IFileDialog_Close","shobjidl_core/IFileDialog::Close"]
old-location: shell\IFileDialog_Close.htm
tech.root: shell
ms.assetid: 064b035a-c554-4c81-93b9-ba4fb92da09d
ms.date: 12/05/2018
ms.keywords: Close, Close method [Windows Shell], Close method [Windows Shell],IFileDialog interface, IFileDialog interface [Windows Shell],Close method, IFileDialog.Close, IFileDialog::Close, shell.IFileDialog_Close, shell_IFileDialog_Close, shobjidl_core/IFileDialog::Close
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
 - IFileDialog::Close
 - shobjidl_core/IFileDialog::Close
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
 - IFileDialog.Close
---

# IFileDialog::Close


## -description

Closes the dialog.

## -parameters

### -param hr [in]

Type: <b>HRESULT</b>

The code that will be returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show">Show</a> to indicate that the dialog was closed before a selection was made.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An application can call this method from a callback method or function while the dialog is open. The dialog will close and the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show">Show</a> method will return with the <b>HRESULT</b> specified in <i>hr</i>.

If this method is called, there is no result available for the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult">IFileDialog::GetResult</a> or <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults">GetResults</a> methods, and they will fail if called.