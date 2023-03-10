---
UID: NF:shobjidl.IFileDialogControlEvents.OnButtonClicked
title: IFileDialogControlEvents::OnButtonClicked (shobjidl.h)
description: Called when the user clicks a command button.
helpviewer_keywords: ["IFileDialogControlEvents interface [Windows Shell]","OnButtonClicked method","IFileDialogControlEvents.OnButtonClicked","IFileDialogControlEvents::OnButtonClicked","OnButtonClicked","OnButtonClicked method [Windows Shell]","OnButtonClicked method [Windows Shell]","IFileDialogControlEvents interface","shell.IFileDialogControlEvents_OnButtonClicked","shell_IFileDialogControlEvents_OnButtonClicked","shobjidl/IFileDialogControlEvents::OnButtonClicked"]
old-location: shell\IFileDialogControlEvents_OnButtonClicked.htm
tech.root: shell
ms.assetid: 46dc28a4-717f-42b6-bff7-56f4902f075c
ms.date: 12/05/2018
ms.keywords: IFileDialogControlEvents interface [Windows Shell],OnButtonClicked method, IFileDialogControlEvents.OnButtonClicked, IFileDialogControlEvents::OnButtonClicked, OnButtonClicked, OnButtonClicked method [Windows Shell], OnButtonClicked method [Windows Shell],IFileDialogControlEvents interface, shell.IFileDialogControlEvents_OnButtonClicked, shell_IFileDialogControlEvents_OnButtonClicked, shobjidl/IFileDialogControlEvents::OnButtonClicked
req.header: shobjidl.h
req.include-header: 
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
 - IFileDialogControlEvents::OnButtonClicked
 - shobjidl/IFileDialogControlEvents::OnButtonClicked
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IFileDialogControlEvents.OnButtonClicked
---

# IFileDialogControlEvents::OnButtonClicked


## -description

Called when the user clicks a command button.

## -parameters

### -param pfdc [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize">IFileDialogCustomize</a>*</b>

A pointer to the interface through which the application added controls to the dialog.

### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the button that the user clicked.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.