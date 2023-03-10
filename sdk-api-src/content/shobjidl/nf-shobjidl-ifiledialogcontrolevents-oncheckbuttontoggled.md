---
UID: NF:shobjidl.IFileDialogControlEvents.OnCheckButtonToggled
title: IFileDialogControlEvents::OnCheckButtonToggled (shobjidl.h)
description: Called when the user changes the state of a check button (check box).
helpviewer_keywords: ["IFileDialogControlEvents interface [Windows Shell]","OnCheckButtonToggled method","IFileDialogControlEvents.OnCheckButtonToggled","IFileDialogControlEvents::OnCheckButtonToggled","OnCheckButtonToggled","OnCheckButtonToggled method [Windows Shell]","OnCheckButtonToggled method [Windows Shell]","IFileDialogControlEvents interface","shell.IFileDialogControlEvents_OnCheckButtonToggled","shell_IFileDialogControlEvents_OnCheckButtonToggled","shobjidl/IFileDialogControlEvents::OnCheckButtonToggled"]
old-location: shell\IFileDialogControlEvents_OnCheckButtonToggled.htm
tech.root: shell
ms.assetid: 97e6cb2a-1ffc-43ca-abb6-f1b259e8fcd2
ms.date: 12/05/2018
ms.keywords: IFileDialogControlEvents interface [Windows Shell],OnCheckButtonToggled method, IFileDialogControlEvents.OnCheckButtonToggled, IFileDialogControlEvents::OnCheckButtonToggled, OnCheckButtonToggled, OnCheckButtonToggled method [Windows Shell], OnCheckButtonToggled method [Windows Shell],IFileDialogControlEvents interface, shell.IFileDialogControlEvents_OnCheckButtonToggled, shell_IFileDialogControlEvents_OnCheckButtonToggled, shobjidl/IFileDialogControlEvents::OnCheckButtonToggled
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
 - IFileDialogControlEvents::OnCheckButtonToggled
 - shobjidl/IFileDialogControlEvents::OnCheckButtonToggled
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
 - IFileDialogControlEvents.OnCheckButtonToggled
---

# IFileDialogControlEvents::OnCheckButtonToggled


## -description

Called when the user changes the state of a check button (check box).

## -parameters

### -param pfdc [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize">IFileDialogCustomize</a>*</b>

A pointer to the interface through which the application added controls to the dialog.

### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the button that the user clicked.

### -param bChecked [in]

Type: <b>BOOL</b>

A <b>BOOL</b> indicating the current state of the check button. <b>TRUE</b> if checked; <b>FALSE</b> otherwise.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.