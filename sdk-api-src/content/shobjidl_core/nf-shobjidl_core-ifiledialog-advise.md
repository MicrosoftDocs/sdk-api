---
UID: NF:shobjidl_core.IFileDialog.Advise
title: IFileDialog::Advise (shobjidl_core.h)
description: Assigns an event handler that listens for events coming from the dialog.
helpviewer_keywords: ["Advise","Advise method [Windows Shell]","Advise method [Windows Shell]","IFileDialog interface","IFileDialog interface [Windows Shell]","Advise method","IFileDialog.Advise","IFileDialog::Advise","shell.IFileDialog_Advise","shell_IFileDialog_Advise","shobjidl_core/IFileDialog::Advise"]
old-location: shell\IFileDialog_Advise.htm
tech.root: shell
ms.assetid: f5664a52-f26c-475d-84ef-0c657ae46e2e
ms.date: 12/05/2018
ms.keywords: Advise, Advise method [Windows Shell], Advise method [Windows Shell],IFileDialog interface, IFileDialog interface [Windows Shell],Advise method, IFileDialog.Advise, IFileDialog::Advise, shell.IFileDialog_Advise, shell_IFileDialog_Advise, shobjidl_core/IFileDialog::Advise
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
 - IFileDialog::Advise
 - shobjidl_core/IFileDialog::Advise
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
 - IFileDialog.Advise
---

# IFileDialog::Advise


## -description

Assigns an event handler that listens for events coming from the dialog.

## -parameters

### -param pfde [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents">IFileDialogEvents</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents">IFileDialogEvents</a> implementation that will receive events from the dialog.

### -param pdwCookie [out]

Type: <b>DWORD*</b>

A pointer to a <b>DWORD</b> that receives a value identifying this event handler. When the client is finished with the dialog, that client must call the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-unadvise">IFileDialog::Unadvise</a> method with this value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.