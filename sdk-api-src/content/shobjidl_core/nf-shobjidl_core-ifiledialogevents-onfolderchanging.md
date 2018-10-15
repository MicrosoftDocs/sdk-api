---
UID: NF:shobjidl_core.IFileDialogEvents.OnFolderChanging
title: IFileDialogEvents::OnFolderChanging
author: windows-sdk-content
description: Called before IFileDialogEvents::OnFolderChange. This allows the implementer to stop navigation to a particular location.
old-location: shell\IFileDialogEvents_OnFolderChanging.htm
tech.root: shell
ms.assetid: 4114ed48-8e1e-4ddf-9434-629b99fc40d9
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IFileDialogEvents interface [Windows Shell],OnFolderChanging method, IFileDialogEvents.OnFolderChanging, IFileDialogEvents::OnFolderChanging, OnFolderChanging, OnFolderChanging method [Windows Shell], OnFolderChanging method [Windows Shell],IFileDialogEvents interface, shell.IFileDialogEvents_OnFolderChanging, shell_IFileDialogEvents_OnFolderChanging, shobjidl_core/IFileDialogEvents::OnFolderChanging
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileDialogEvents.OnFolderChanging
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileDialogEvents::OnFolderChanging


## -description


Called before <a href="https://msdn.microsoft.com/3e5ec923-0597-4cf4-8973-17c83481c7f4">IFileDialogEvents::OnFolderChange</a>. This allows the implementer to stop navigation to a particular location.


## -parameters




### -param pfd [in]

Type: <b><a href="https://msdn.microsoft.com/9341bb68-2410-4e03-8acd-fef29287b61c">IFileDialog</a>*</b>

A pointer to the interface that represents the dialog.


### -param psiFolder [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to an interface that represents the folder to which the dialog is about to navigate.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. A return value of S_OK or E_NOTIMPL indicates that the folder change can proceed.




## -remarks



The calling application can call <a href="https://msdn.microsoft.com/3f300c70-cae8-43bb-95d4-25ac4be9b4c4">IFileDialog::SetFolder</a> during this callback to redirect navigation to an alternate folder. The actual navigation does not occur until <b>IFileDialogEvents::OnFolderChanging</b> has returned.

If the calling application simply prevents navigation to a particular folder, UI should be displayed with an explanation of the restriction. To obtain a parent <b>HWND</b> for the UI, obtain the <a href="https://msdn.microsoft.com/2d0efbae-4a1c-43b1-9021-8d89377f7282">IOleWindow</a> interface through <a href="https://msdn.microsoft.com/9341bb68-2410-4e03-8acd-fef29287b61c">IFileDialog</a> and call <a href="https://msdn.microsoft.com/833adc81-be58-44a1-88f1-9aa28808e67b">IOleWindow::GetWindow</a>.
            



