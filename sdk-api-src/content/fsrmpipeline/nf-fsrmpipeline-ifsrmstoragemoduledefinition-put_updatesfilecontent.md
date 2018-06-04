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

# IFsrmStorageModuleDefinition::put_UpdatesFileContent


## -description


Determines whether the module updates the contents of the file.

This property is read/write.


## -parameters


## -remarks



Setting this property to <b>VARIANT_TRUE</b> does not require that the 
    <a href="https://msdn.microsoft.com/4c4aaacf-d121-412c-9152-5787f351c19c">IFsrmStorageModuleDefinition::StorageType</a> 
    property to be set to <b>FsrmStorageModuleType_InFile</b>. For example, you can set this 
    property to <b>VARIANT_TRUE</b> if you need to update the file to let another process know that 
    you have processed the file.




## -see-also




<a href="https://msdn.microsoft.com/68ecb5e6-61b0-488f-b6bb-181f253de70e">IFsrmStorageModuleDefinition</a>
 

 

