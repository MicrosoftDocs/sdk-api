---
UID: NF:shobjidl.IFileDialogControlEvents.OnItemSelected
title: IFileDialogControlEvents::OnItemSelected (shobjidl.h)
description: Called when an item is selected in a combo box, when a user clicks an option button (also known as a radio button), or an item is chosen from the Tools menu.
helpviewer_keywords: ["IFileDialogControlEvents interface [Windows Shell]","OnItemSelected method","IFileDialogControlEvents.OnItemSelected","IFileDialogControlEvents::OnItemSelected","OnItemSelected","OnItemSelected method [Windows Shell]","OnItemSelected method [Windows Shell]","IFileDialogControlEvents interface","shell.IFileDialogControlEvents_OnItemSelected","shell_IFileDialogControlEvents_OnItemSelected","shobjidl/IFileDialogControlEvents::OnItemSelected"]
old-location: shell\IFileDialogControlEvents_OnItemSelected.htm
tech.root: shell
ms.assetid: 4c96d0b7-74d1-4f87-946d-beeaad517d91
ms.date: 12/05/2018
ms.keywords: IFileDialogControlEvents interface [Windows Shell],OnItemSelected method, IFileDialogControlEvents.OnItemSelected, IFileDialogControlEvents::OnItemSelected, OnItemSelected, OnItemSelected method [Windows Shell], OnItemSelected method [Windows Shell],IFileDialogControlEvents interface, shell.IFileDialogControlEvents_OnItemSelected, shell_IFileDialogControlEvents_OnItemSelected, shobjidl/IFileDialogControlEvents::OnItemSelected
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
 - IFileDialogControlEvents::OnItemSelected
 - shobjidl/IFileDialogControlEvents::OnItemSelected
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
 - IFileDialogControlEvents.OnItemSelected
---

# IFileDialogControlEvents::OnItemSelected


## -description

Called when an item is selected in a combo box, when a user clicks an option button (also known as a radio button), or an item is chosen from the <b>Tools</b> menu.

## -parameters

### -param pfdc [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize">IFileDialogCustomize</a>*</b>

A pointer to the interface through which the application added controls to the dialog.

### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the control in which the user made a selection.

### -param dwIDItem [in]

Type: <b>DWORD</b>

The ID of the selection.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This notification is not sent when the user chooses an item from the drop-down menu attached to the <b>Open</b> button, because the action taken in that case is always the same: close the dialog as if the user had simply clicked the <b>Open</b> button. For that situation, the application can call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-getselectedcontrolitem">GetSelectedControlItem</a> to obtain the item the user chose from that menu.