---
UID: NF:shobjidl_core.IFileDialogCustomize.SetControlState
title: IFileDialogCustomize::SetControlState
author: windows-sdk-content
description: Sets the current visibility and enabled states of a given control.
old-location: shell\IFileDialogCustomize_SetControlState.htm
old-project: shell
ms.assetid: 53b9a65d-2219-45d0-9367-b9ea3e87cd70
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IFileDialogCustomize interface [Windows Shell],SetControlState method, IFileDialogCustomize.SetControlState, IFileDialogCustomize::SetControlState, SetControlState, SetControlState method [Windows Shell], SetControlState method [Windows Shell],IFileDialogCustomize interface, shell.IFileDialogCustomize_SetControlState, shell_IFileDialogCustomize_SetControlState, shobjidl_core/IFileDialogCustomize::SetControlState
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileDialogCustomize.SetControlState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileDialogCustomize::SetControlState


## -description


Sets the current visibility and enabled states of a given control.


## -parameters




### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the control in question.


### -param dwState






#### - pdwState [in]

Type: <b>CDCONTROLSTATEF</b>

One or more values from the <a href="https://msdn.microsoft.com/5e556aa2-2e1b-4f71-b386-328405f4aae0">CDCONTROLSTATE</a> enumeration that indicate the current state of the control.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When the dialog is shown, controls cannot be added or removed, but the existing controls can be hidden or disabled at any time.



