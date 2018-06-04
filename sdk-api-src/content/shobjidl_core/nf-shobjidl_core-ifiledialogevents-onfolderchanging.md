---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
            



