---
UID: NF:shobjidl_core.IFileDialogEvents.OnFileOk
title: IFileDialogEvents::OnFileOk (shobjidl_core.h)
description: Called just before the dialog is about to return with a result.
helpviewer_keywords: ["IFileDialogEvents interface [Windows Shell]","OnFileOk method","IFileDialogEvents.OnFileOk","IFileDialogEvents::OnFileOk","OnFileOk","OnFileOk method [Windows Shell]","OnFileOk method [Windows Shell]","IFileDialogEvents interface","shell.IFileDialogEvents_OnFileOk","shell_IFileDialogEvents_OnFileOk","shobjidl_core/IFileDialogEvents::OnFileOk"]
old-location: shell\IFileDialogEvents_OnFileOk.htm
tech.root: shell
ms.assetid: 81277122-b2fe-40af-85f8-d578925856a1
ms.date: 12/05/2018
ms.keywords: IFileDialogEvents interface [Windows Shell],OnFileOk method, IFileDialogEvents.OnFileOk, IFileDialogEvents::OnFileOk, OnFileOk, OnFileOk method [Windows Shell], OnFileOk method [Windows Shell],IFileDialogEvents interface, shell.IFileDialogEvents_OnFileOk, shell_IFileDialogEvents_OnFileOk, shobjidl_core/IFileDialogEvents::OnFileOk
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
 - IFileDialogEvents::OnFileOk
 - shobjidl_core/IFileDialogEvents::OnFileOk
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
 - IFileDialogEvents.OnFileOk
---

# IFileDialogEvents::OnFileOk


## -description

Called just before the dialog is about to return with a result.

## -parameters

### -param pfd [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a>*</b>

A pointer to the interface that represents the dialog.

## -returns

Type: <b>HRESULT</b>

Implementations should return <b>S_OK</b> to accept the current result in the dialog or <b>S_FALSE</b> to refuse it. In the case of <b>S_FALSE</b>, the dialog should remain open.

## -remarks

When this method is called, the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult">IFileDialog::GetResult</a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults">GetResults</a> methods can be called.

The application can use this callback method to perform additional validation before the dialog closes, or to prevent the dialog from closing. If the application prevents the dialog from closing, it should display a UI to indicate a cause. To obtain a parent <b>HWND</b> for the UI, obtain the <a href="/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a> interface through <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IFileDialog::QueryInterface</a> and call <a href="/windows/desktop/api/oleidl/nf-oleidl-iolewindow-getwindow">IOleWindow::GetWindow</a>.

An application can also use this method to perform all of its work surrounding the opening or saving of files.