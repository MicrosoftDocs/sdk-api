---
UID: NF:shobjidl_core.IFileDialogEvents.OnTypeChange
title: IFileDialogEvents::OnTypeChange (shobjidl_core.h)
description: Called when the dialog is opened to notify the application of the initial chosen filetype.
helpviewer_keywords: ["IFileDialogEvents interface [Windows Shell]","OnTypeChange method","IFileDialogEvents.OnTypeChange","IFileDialogEvents::OnTypeChange","OnTypeChange","OnTypeChange method [Windows Shell]","OnTypeChange method [Windows Shell]","IFileDialogEvents interface","shell.IFileDialogEvents_OnTypeChange","shell_IFileDialogEvents_OnTypeChange","shobjidl_core/IFileDialogEvents::OnTypeChange"]
old-location: shell\IFileDialogEvents_OnTypeChange.htm
tech.root: shell
ms.assetid: d57e7b57-520d-40d6-8bac-ebf245ad7484
ms.date: 12/05/2018
ms.keywords: IFileDialogEvents interface [Windows Shell],OnTypeChange method, IFileDialogEvents.OnTypeChange, IFileDialogEvents::OnTypeChange, OnTypeChange, OnTypeChange method [Windows Shell], OnTypeChange method [Windows Shell],IFileDialogEvents interface, shell.IFileDialogEvents_OnTypeChange, shell_IFileDialogEvents_OnTypeChange, shobjidl_core/IFileDialogEvents::OnTypeChange
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
 - IFileDialogEvents::OnTypeChange
 - shobjidl_core/IFileDialogEvents::OnTypeChange
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
 - IFileDialogEvents.OnTypeChange
---

# IFileDialogEvents::OnTypeChange


## -description

Called when the dialog is opened to notify the application of the initial chosen filetype.

## -parameters

### -param pfd [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a>*</b>

A pointer to the interface that represents the dialog.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is called when the dialog is opened to notify the application of the initially chosen filetype. If the application has code in <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents">IFileDialogEvents</a> that responds to type changes, it can respond to the type. For example, it could hide certain controls. The application controls the initial file type and could do its own checks, so this method is provided as a convenience.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/bb775958(v=vs.85)">IFileDialog::GetFileTypeIndex</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents">IFileDialogEvents</a>