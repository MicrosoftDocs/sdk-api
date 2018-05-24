---
UID: NF:shobjidl_core.IFileDialogCustomize.AddSeparator
title: IFileDialogCustomize::AddSeparator
author: windows-driver-content
description: Adds a separator to the dialog, allowing a visual separation of controls.
old-location: shell\IFileDialogCustomize_AddSeparator.htm
old-project: shell
ms.assetid: e2d0f1c7-9296-4651-8910-89dcfe5a6a68
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: AddSeparator, AddSeparator method [Windows Shell], AddSeparator method [Windows Shell],IFileDialogCustomize interface, IFileDialogCustomize interface [Windows Shell],AddSeparator method, IFileDialogCustomize.AddSeparator, IFileDialogCustomize::AddSeparator, shell.IFileDialogCustomize_AddSeparator, shell_IFileDialogCustomize_AddSeparator, shobjidl_core/IFileDialogCustomize::AddSeparator
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IFileDialogCustomize.AddSeparator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileDialogCustomize::AddSeparator


## -description


Adds a separator to the dialog, allowing a visual separation of controls.


## -parameters




### -param dwIDCtl [in]

Type: <b>DWORD</b>

The control ID of the separator.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The default state for this control is enabled and visible.



