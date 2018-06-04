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

# IFsrmFileScreenManager::EnumFileScreens


## -description


Enumerates the file screens for the specified directory and its subdirectories.


## -parameters




### -param path [in]

The local directory path associated with the file screen that you want to retrieve.

If the path ends with "\*", retrieve all file screens associated with the immediate subdirectories of the path (does not include the file screen associated with the path).

If the path ends with "\...", retrieve the file screen for the path and all file screens associated with the immediate subdirectories of the path (recursively).

If the path does not end in "\*" or "\...", retrieve the file screen for the path only.

If path is null or empty, the method returns all file screens.


### -param options [in]

The options to use when enumerating the file screens. For possible values, see the <a href="https://msdn.microsoft.com/9c613d0c-c49a-4010-b66f-a63c57d693f7">FsrmEnumOptions</a> enumeration.


### -param fileScreens [out]

An <a href="https://msdn.microsoft.com/ef4678b4-e6b0-4044-ba11-7a3ae01ad2c7">IFsrmCommittableCollection</a> interface that contains a collection of file screens.

Each item of the collection is a <b>VARIANT</b> of type <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant for the <a href="https://msdn.microsoft.com/69b831a1-c935-4de0-b222-009bafc45ec5">IFsrmFileScreen</a> interface.

The collection contains only committed file screens; the collection will not contain newly created file screens that have not been committed.

The collection is empty if the path does not contain file screens.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/82ff65fa-2e82-4f07-bdd4-e3b01d184c16">FsrmFileScreenManager</a>



<a href="https://msdn.microsoft.com/a0cea95d-5839-41a2-91b9-da8e13030682">IFsrmFileScreenManager</a>
 

 

