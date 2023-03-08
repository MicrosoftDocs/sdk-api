---
UID: NF:shobjidl_core.IFileDialogEvents.OnSelectionChange
title: IFileDialogEvents::OnSelectionChange (shobjidl_core.h)
description: Called when the user changes the selection in the dialog's view.
helpviewer_keywords: ["IFileDialogEvents interface [Windows Shell]","OnSelectionChange method","IFileDialogEvents.OnSelectionChange","IFileDialogEvents::OnSelectionChange","OnSelectionChange","OnSelectionChange method [Windows Shell]","OnSelectionChange method [Windows Shell]","IFileDialogEvents interface","shell.IFileDialogEvents_OnSelectionChange","shell_IFileDialogEvents_OnSelectionChange","shobjidl_core/IFileDialogEvents::OnSelectionChange"]
old-location: shell\IFileDialogEvents_OnSelectionChange.htm
tech.root: shell
ms.assetid: 5fd69b1f-4e4b-4643-8429-9b5f98f3d702
ms.date: 12/05/2018
ms.keywords: IFileDialogEvents interface [Windows Shell],OnSelectionChange method, IFileDialogEvents.OnSelectionChange, IFileDialogEvents::OnSelectionChange, OnSelectionChange, OnSelectionChange method [Windows Shell], OnSelectionChange method [Windows Shell],IFileDialogEvents interface, shell.IFileDialogEvents_OnSelectionChange, shell_IFileDialogEvents_OnSelectionChange, shobjidl_core/IFileDialogEvents::OnSelectionChange
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
 - IFileDialogEvents::OnSelectionChange
 - shobjidl_core/IFileDialogEvents::OnSelectionChange
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
 - IFileDialogEvents.OnSelectionChange
---

# IFileDialogEvents::OnSelectionChange


## -description

Called when the user changes the selection in the dialog's view.

## -parameters

### -param pfd [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a>*</b>

A pointer to the interface that represents the dialog.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.