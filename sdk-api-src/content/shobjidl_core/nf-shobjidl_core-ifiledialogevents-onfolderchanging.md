---
UID: NF:shobjidl_core.IFileDialogEvents.OnFolderChanging
title: IFileDialogEvents::OnFolderChanging (shobjidl_core.h)
description: Called before IFileDialogEvents::OnFolderChange. This allows the implementer to stop navigation to a particular location.
helpviewer_keywords: ["IFileDialogEvents interface [Windows Shell]","OnFolderChanging method","IFileDialogEvents.OnFolderChanging","IFileDialogEvents::OnFolderChanging","OnFolderChanging","OnFolderChanging method [Windows Shell]","OnFolderChanging method [Windows Shell]","IFileDialogEvents interface","shell.IFileDialogEvents_OnFolderChanging","shell_IFileDialogEvents_OnFolderChanging","shobjidl_core/IFileDialogEvents::OnFolderChanging"]
old-location: shell\IFileDialogEvents_OnFolderChanging.htm
tech.root: shell
ms.assetid: 4114ed48-8e1e-4ddf-9434-629b99fc40d9
ms.date: 12/05/2018
ms.keywords: IFileDialogEvents interface [Windows Shell],OnFolderChanging method, IFileDialogEvents.OnFolderChanging, IFileDialogEvents::OnFolderChanging, OnFolderChanging, OnFolderChanging method [Windows Shell], OnFolderChanging method [Windows Shell],IFileDialogEvents interface, shell.IFileDialogEvents_OnFolderChanging, shell_IFileDialogEvents_OnFolderChanging, shobjidl_core/IFileDialogEvents::OnFolderChanging
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
 - IFileDialogEvents::OnFolderChanging
 - shobjidl_core/IFileDialogEvents::OnFolderChanging
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
 - IFileDialogEvents.OnFolderChanging
---

# IFileDialogEvents::OnFolderChanging


## -description

Called before <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfolderchange">IFileDialogEvents::OnFolderChange</a>. This allows the implementer to stop navigation to a particular location.

## -parameters

### -param pfd [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a>*</b>

A pointer to the interface that represents the dialog.

### -param psiFolder [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to an interface that represents the folder to which the dialog is about to navigate.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. A return value of S_OK or E_NOTIMPL indicates that the folder change can proceed.

## -remarks

The calling application can call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfolder">IFileDialog::SetFolder</a> during this callback to redirect navigation to an alternate folder. The actual navigation does not occur until <b>IFileDialogEvents::OnFolderChanging</b> has returned.

If the calling application simply prevents navigation to a particular folder, UI should be displayed with an explanation of the restriction. To obtain a parent <b>HWND</b> for the UI, obtain the <a href="/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a> interface through <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a> and call <a href="/windows/desktop/api/oleidl/nf-oleidl-iolewindow-getwindow">IOleWindow::GetWindow</a>.