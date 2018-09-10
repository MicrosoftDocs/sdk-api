---
UID: NF:shobjidl_core.IFileDialogEvents.OnFolderChange
title: IFileDialogEvents::OnFolderChange
author: windows-sdk-content
description: Called when the user navigates to a new folder.
old-location: shell\IFileDialogEvents_OnFolderChange.htm
tech.root: shell
ms.assetid: 3e5ec923-0597-4cf4-8973-17c83481c7f4
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IFileDialogEvents interface [Windows Shell],OnFolderChange method, IFileDialogEvents.OnFolderChange, IFileDialogEvents::OnFolderChange, OnFolderChange, OnFolderChange method [Windows Shell], OnFolderChange method [Windows Shell],IFileDialogEvents interface, shell.IFileDialogEvents_OnFolderChange, shell_IFileDialogEvents_OnFolderChange, shobjidl_core/IFileDialogEvents::OnFolderChange
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
 - IFileDialogEvents.OnFolderChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileDialogEvents::OnFolderChange


## -description


Called when the user navigates to a new folder.


## -parameters




### -param pfd [in]

Type: <b><a href="https://msdn.microsoft.com/9341bb68-2410-4e03-8acd-fef29287b61c">IFileDialog</a>*</b>

A pointer to the interface that represents the dialog.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IFileDialogEvents::OnFolderChange</b> is called when the dialog is opened.




## -see-also




<a href="https://msdn.microsoft.com/424d1507-e42a-43d7-8904-347bfb311dd4">IFileDialog::GetFolder</a>



<a href="https://msdn.microsoft.com/c55107a3-ae0a-4b46-80a3-8a731b47976c">IFileDialogEvents</a>



<a href="https://msdn.microsoft.com/4114ed48-8e1e-4ddf-9434-629b99fc40d9">IFileDialogEvents::OnFolderChanging</a>
 

 

