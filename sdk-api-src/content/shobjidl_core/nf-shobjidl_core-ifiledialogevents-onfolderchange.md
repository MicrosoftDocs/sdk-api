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
 

 

