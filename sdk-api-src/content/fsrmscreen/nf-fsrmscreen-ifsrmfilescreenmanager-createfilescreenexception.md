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

# IFsrmFileScreenManager::CreateFileScreenException


## -description


Creates a file screen exception object.


## -parameters




### -param path [in]

The local directory path to which the file screen exception applies. The path is limited to 260 characters.


### -param fileScreenException [out]

An <a href="https://msdn.microsoft.com/188e76dd-6df6-412f-8d51-fc727075de80">IFsrmFileScreenException</a> interface of the newly created file screen exception. To add the exception to FSRM, call <a href="https://msdn.microsoft.com/81c9b1db-7756-47b2-98e6-8e819d93cd0f">IFsrmFileScreenException::Commit</a> method.


## -returns



The method returns the following return values.




## -remarks



You can use the exception to allow files to be saved in a directory when a file screen would otherwise prevent it. For example, if P:\<i>directory</i> contains a file screen that blocks *.mp3, you could create an exception that allows MP3 files on P:\<i>directory</i>\<i>subdirectory</i>.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/a046f092-5b6d-452d-826b-fd4b83c774fb">Defining a File Screen Exception</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/82ff65fa-2e82-4f07-bdd4-e3b01d184c16">FsrmFileScreenManager</a>



<a href="https://msdn.microsoft.com/a0cea95d-5839-41a2-91b9-da8e13030682">IFsrmFileScreenManager</a>
 

 

