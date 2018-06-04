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

# IApplicationActivationManager::ActivateForFile


## -description


Activates the specified Windows Store app for the file contract (Windows.File).


## -parameters




### -param appUserModelId [in]

The application user model ID of the Windows Store app.


### -param itemArray [in]

A pointer to an array of Shell items, each representing a file. This value is converted to a <a href="https://msdn.microsoft.com/313dd554-73a7-42e7-9321-9b00927ca33d">VectorView</a> of <a href="https://msdn.microsoft.com/552d3c28-b93a-487f-9698-886a52fa7c97">StorageItem</a> objects that is passed to the app through <a href="https://msdn.microsoft.com/511fcaf9-b3de-4f62-a26f-92a5b0575fd7">FileActivatedEventArgs</a>.


### -param verb [in]

The verb being applied to the file or files specified by <i>itemArray</i>.


### -param processId [out]

A pointer to a value that, when this method returns successfully, receives the process ID of the app instance that fulfils this contract.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/66C8EDC8-AF05-46d6-B29D-B6EE09DF6709">IApplicationActivationManager</a>
 

 

