---
UID: NF:shobjidl.IFileDialogControlEvents.OnControlActivating
title: IFileDialogControlEvents::OnControlActivating (shobjidl.h)
description: Called when an Open button drop-down list customized through EnableOpenDropDown or a Tools menu is about to display its contents.
helpviewer_keywords: ["IFileDialogControlEvents interface [Windows Shell]","OnControlActivating method","IFileDialogControlEvents.OnControlActivating","IFileDialogControlEvents::OnControlActivating","OnControlActivating","OnControlActivating method [Windows Shell]","OnControlActivating method [Windows Shell]","IFileDialogControlEvents interface","shell.IFileDialogControlEvents_OnControlActivating","shell_IFileDialogControlEvents_OnControlActivating","shobjidl/IFileDialogControlEvents::OnControlActivating"]
old-location: shell\IFileDialogControlEvents_OnControlActivating.htm
tech.root: shell
ms.assetid: 12efb183-65b9-4095-be57-7c7802bda2ce
ms.date: 12/05/2018
ms.keywords: IFileDialogControlEvents interface [Windows Shell],OnControlActivating method, IFileDialogControlEvents.OnControlActivating, IFileDialogControlEvents::OnControlActivating, OnControlActivating, OnControlActivating method [Windows Shell], OnControlActivating method [Windows Shell],IFileDialogControlEvents interface, shell.IFileDialogControlEvents_OnControlActivating, shell_IFileDialogControlEvents_OnControlActivating, shobjidl/IFileDialogControlEvents::OnControlActivating
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
 - IFileDialogControlEvents::OnControlActivating
 - shobjidl/IFileDialogControlEvents::OnControlActivating
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
 - IFileDialogControlEvents.OnControlActivating
---

# IFileDialogControlEvents::OnControlActivating


## -description

Called when an <b>Open</b> button drop-down list customized through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-enableopendropdown">EnableOpenDropDown</a> or a <b>Tools</b> menu is about to display its contents.

## -parameters

### -param pfdc [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize">IFileDialogCustomize</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize">IFileDialogCustomize</a> object through which the application adds controls to the dialog.

### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the list or menu about to display.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

In response to this notification, an application can update the contents of the menu or list about to be displayed, based on the current state of the dialog.