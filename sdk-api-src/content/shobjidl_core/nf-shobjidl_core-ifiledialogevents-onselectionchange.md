---
UID: NF:shobjidl_core.IFileDialogEvents.OnSelectionChange
title: IFileDialogEvents::OnSelectionChange
author: windows-sdk-content
description: Called when the user changes the selection in the dialog's view.
old-location: shell\IFileDialogEvents_OnSelectionChange.htm
old-project: shell
ms.assetid: 5fd69b1f-4e4b-4643-8429-9b5f98f3d702
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IFileDialogEvents interface [Windows Shell],OnSelectionChange method, IFileDialogEvents.OnSelectionChange, IFileDialogEvents::OnSelectionChange, OnSelectionChange, OnSelectionChange method [Windows Shell], OnSelectionChange method [Windows Shell],IFileDialogEvents interface, shell.IFileDialogEvents_OnSelectionChange, shell_IFileDialogEvents_OnSelectionChange, shobjidl_core/IFileDialogEvents::OnSelectionChange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
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
 - IFileDialogEvents.OnSelectionChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileDialogEvents::OnSelectionChange


## -description


Called when the user changes the selection in the dialog's view.


## -parameters




### -param pfd [in]

Type: <b><a href="https://msdn.microsoft.com/9341bb68-2410-4e03-8acd-fef29287b61c">IFileDialog</a>*</b>

A pointer to the interface that represents the dialog.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



