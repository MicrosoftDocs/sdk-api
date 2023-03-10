---
UID: NF:shobjidl_core.IFileDialogCustomize.GetControlState
title: IFileDialogCustomize::GetControlState (shobjidl_core.h)
description: Gets the current visibility and enabled states of a given control.
helpviewer_keywords: ["GetControlState","GetControlState method [Windows Shell]","GetControlState method [Windows Shell]","IFileDialogCustomize interface","IFileDialogCustomize interface [Windows Shell]","GetControlState method","IFileDialogCustomize.GetControlState","IFileDialogCustomize::GetControlState","shell.IFileDialogCustomize_GetControlState","shell_IFileDialogCustomize_GetControlState","shobjidl_core/IFileDialogCustomize::GetControlState"]
old-location: shell\IFileDialogCustomize_GetControlState.htm
tech.root: shell
ms.assetid: 2a167050-2778-4cc2-9b05-ec81f679c6c0
ms.date: 12/05/2018
ms.keywords: GetControlState, GetControlState method [Windows Shell], GetControlState method [Windows Shell],IFileDialogCustomize interface, IFileDialogCustomize interface [Windows Shell],GetControlState method, IFileDialogCustomize.GetControlState, IFileDialogCustomize::GetControlState, shell.IFileDialogCustomize_GetControlState, shell_IFileDialogCustomize_GetControlState, shobjidl_core/IFileDialogCustomize::GetControlState
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
 - IFileDialogCustomize::GetControlState
 - shobjidl_core/IFileDialogCustomize::GetControlState
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
 - IFileDialogCustomize.GetControlState
---

# IFileDialogCustomize::GetControlState


## -description

Gets the current visibility and enabled states of a given control.

## -parameters

### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the control in question.

### -param pdwState [out]

Type: <b>CDCONTROLSTATEF*</b>

A pointer to a variable that receives one or more values from the <a href="/previous-versions/windows/desktop/legacy/bb762483(v=vs.85)">CDCONTROLSTATE</a> enumeration that indicate the current state of the control.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.