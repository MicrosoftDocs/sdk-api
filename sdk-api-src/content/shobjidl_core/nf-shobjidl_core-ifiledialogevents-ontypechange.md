---
UID: NF:shobjidl_core.IFileDialogEvents.OnTypeChange
title: IFileDialogEvents::OnTypeChange
author: windows-sdk-content
description: Called when the dialog is opened to notify the application of the initial chosen filetype.
old-location: shell\IFileDialogEvents_OnTypeChange.htm
old-project: shell
ms.assetid: d57e7b57-520d-40d6-8bac-ebf245ad7484
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IFileDialogEvents interface [Windows Shell],OnTypeChange method, IFileDialogEvents.OnTypeChange, IFileDialogEvents::OnTypeChange, OnTypeChange, OnTypeChange method [Windows Shell], OnTypeChange method [Windows Shell],IFileDialogEvents interface, shell.IFileDialogEvents_OnTypeChange, shell_IFileDialogEvents_OnTypeChange, shobjidl_core/IFileDialogEvents::OnTypeChange
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IFileDialogEvents.OnTypeChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileDialogEvents::OnTypeChange


## -description


Called when the dialog is opened to notify the application of the initial chosen filetype.


## -parameters




### -param pfd [in]

Type: <b><a href="https://msdn.microsoft.com/9341bb68-2410-4e03-8acd-fef29287b61c">IFileDialog</a>*</b>

A pointer to the interface that represents the dialog.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




              This method is called when the dialog is opened to notify the application of the initially chosen filetype. If the application has code in <a href="https://msdn.microsoft.com/c55107a3-ae0a-4b46-80a3-8a731b47976c">IFileDialogEvents</a> that responds to type changes, it can respond to the type. For example, it could hide certain controls. The application controls the initial file type and could do its own checks, so this method is provided as a convenience.
            




## -see-also




<a href="https://msdn.microsoft.com/ae5b08a1-a97d-433b-88dc-938abe028384">IFileDialog::GetFileTypeIndex</a>



<a href="https://msdn.microsoft.com/c55107a3-ae0a-4b46-80a3-8a731b47976c">IFileDialogEvents</a>
 

 

