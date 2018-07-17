---
UID: NF:shobjidl_core.IFileDialogCustomize.GetControlState
title: IFileDialogCustomize::GetControlState
author: windows-sdk-content
description: Gets the current visibility and enabled states of a given control.
old-location: shell\IFileDialogCustomize_GetControlState.htm
old-project: shell
ms.assetid: 2a167050-2778-4cc2-9b05-ec81f679c6c0
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetControlState, GetControlState method [Windows Shell], GetControlState method [Windows Shell],IFileDialogCustomize interface, IFileDialogCustomize interface [Windows Shell],GetControlState method, IFileDialogCustomize.GetControlState, IFileDialogCustomize::GetControlState, shell.IFileDialogCustomize_GetControlState, shell_IFileDialogCustomize_GetControlState, shobjidl_core/IFileDialogCustomize::GetControlState
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
 - IFileDialogCustomize.GetControlState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
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

A pointer to a variable that receives one or more values from the <a href="https://msdn.microsoft.com/5e556aa2-2e1b-4f71-b386-328405f4aae0">CDCONTROLSTATE</a> enumeration that indicate the current state of the control.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



