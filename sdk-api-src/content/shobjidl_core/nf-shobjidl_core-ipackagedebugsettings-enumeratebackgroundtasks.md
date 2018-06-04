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

# IPackageDebugSettings::EnumerateBackgroundTasks


## -description


Gets the background tasks that are provided by the specified package.


## -parameters




### -param packageFullName [in]

The package full name to query for background tasks.


### -param taskCount [out]

The count of <i>taskIds</i> and <i>taskNames</i> entries.


### -param taskIds [out]

An array of background task identifiers. You can use these identifiers in the <a href="https://msdn.microsoft.com/30ef83f0-cad1-4aee-9b70-0fe7189aff9e">ActivateBackgroundTask</a> method to activate specified tasks.


### -param taskNames [out]

An array of task names that corresponds with background <i>taskIds</i>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Both parameters <i>taskIds</i> and <i>taskNames</i> have the same ordering of tasks. If you need to know the user-readable task name associated with <i>taskId[0]</i>, refer to <i>taskNames[0]</i>.




## -see-also




<a href="https://msdn.microsoft.com/e407c4ca-0de1-4b17-bb83-5c4128952d48">IPackageDebugSettings</a>
 

 

