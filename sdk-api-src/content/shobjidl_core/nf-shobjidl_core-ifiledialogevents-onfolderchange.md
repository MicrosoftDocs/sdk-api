---
UID: NF:shobjidl_core.IFileDialogEvents.OnFolderChange
title: IFileDialogEvents::OnFolderChange (shobjidl_core.h)
description: Called when the user navigates to a new folder.helpviewer_keywords: ["IFileDialogEvents interface [Windows Shell]","OnFolderChange method","IFileDialogEvents.OnFolderChange","IFileDialogEvents::OnFolderChange","OnFolderChange","OnFolderChange method [Windows Shell]","OnFolderChange method [Windows Shell]","IFileDialogEvents interface","shell.IFileDialogEvents_OnFolderChange","shell_IFileDialogEvents_OnFolderChange","shobjidl_core/IFileDialogEvents::OnFolderChange"]
old-location: shell\IFileDialogEvents_OnFolderChange.htm
tech.root: shell
ms.assetid: 3e5ec923-0597-4cf4-8973-17c83481c7f4
ms.date: 12/05/2018
ms.keywords: IFileDialogEvents interface [Windows Shell],OnFolderChange method, IFileDialogEvents.OnFolderChange, IFileDialogEvents::OnFolderChange, OnFolderChange, OnFolderChange method [Windows Shell], OnFolderChange method [Windows Shell],IFileDialogEvents interface, shell.IFileDialogEvents_OnFolderChange, shell_IFileDialogEvents_OnFolderChange, shobjidl_core/IFileDialogEvents::OnFolderChange
f1_keywords:
- shobjidl_core/IFileDialogEvents.OnFolderChange
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- shobjidl_core.h
api_name:
- IFileDialogEvents.OnFolderChange
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFileDialogEvents::OnFolderChange


## -description


Called when the user navigates to a new folder.


## -parameters




### -param pfd [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a>*</b>

A pointer to the interface that represents the dialog.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IFileDialogEvents::OnFolderChange</b> is called when the dialog is opened.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getfolder">IFileDialog::GetFolder</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents">IFileDialogEvents</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfolderchanging">IFileDialogEvents::OnFolderChanging</a>
 

 

