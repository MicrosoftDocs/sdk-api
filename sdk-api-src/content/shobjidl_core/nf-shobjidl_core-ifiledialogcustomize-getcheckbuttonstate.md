---
UID: NF:shobjidl_core.IFileDialogCustomize.GetCheckButtonState
title: IFileDialogCustomize::GetCheckButtonState
author: windows-sdk-content
description: Gets the current state of a check button (check box) in the dialog.
old-location: shell\IFileDialogCustomize_GetCheckButtonState.htm
old-project: shell
ms.assetid: c16643e5-a711-455a-8967-2c810e28ea60
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: GetCheckButtonState, GetCheckButtonState method [Windows Shell], GetCheckButtonState method [Windows Shell],IFileDialogCustomize interface, IFileDialogCustomize interface [Windows Shell],GetCheckButtonState method, IFileDialogCustomize.GetCheckButtonState, IFileDialogCustomize::GetCheckButtonState, shell.IFileDialogCustomize_GetCheckButtonState, shell_IFileDialogCustomize_GetCheckButtonState, shobjidl_core/IFileDialogCustomize::GetCheckButtonState
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
 - IFileDialogCustomize.GetCheckButtonState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileDialogCustomize::GetCheckButtonState


## -description


Gets the current state of a check button (check box) in the dialog.


## -parameters




### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the check box.


### -param pbChecked [out]

Type: <b>BOOL*</b>

The address of a <b>BOOL</b> value that indicates whether the box is checked. <b>TRUE</b> means checked; <b>FALSE</b>, unchecked.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



