---
UID: NF:shobjidl_core.IFileDialogCustomize.AddPushButton
title: IFileDialogCustomize::AddPushButton
author: windows-sdk-content
description: Adds a button to the dialog.
old-location: shell\IFileDialogCustomize_AddPushButton.htm
old-project: shell
ms.assetid: cd0e4a8f-59c7-4056-8521-abb4c8c08a40
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: AddPushButton, AddPushButton method [Windows Shell], AddPushButton method [Windows Shell],IFileDialogCustomize interface, IFileDialogCustomize interface [Windows Shell],AddPushButton method, IFileDialogCustomize.AddPushButton, IFileDialogCustomize::AddPushButton, shell.IFileDialogCustomize_AddPushButton, shell_IFileDialogCustomize_AddPushButton, shobjidl_core/IFileDialogCustomize::AddPushButton
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
 - IFileDialogCustomize.AddPushButton
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileDialogCustomize::AddPushButton


## -description


Adds a button to the dialog.


## -parameters




### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the button to add.


### -param pszLabel [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the button text as a null-terminated Unicode string.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The default state for this control is enabled and visible.



