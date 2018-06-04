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

# IDataManager::Run


## -description


Manually runs the data manager. 


## -parameters




### -param Steps [in]

Determines whether the folder actions and resource policies are applied and how to generate the report. For possible steps, see the <a href="https://msdn.microsoft.com/e647987d-e524-475e-a355-539cb3f04635">DataManagerSteps</a> enumeration.


### -param bstrFolder [in]

The folder under the <a href="https://msdn.microsoft.com/42940cec-c76a-433c-9308-f030dacb05a4">IDataCollectorSet::RootPath</a> property that contains the files used to generate the report. If <b>NULL</b>, PLA uses all the files in the collection. This folder is used only if the <i>Steps</i> parameter includes <b>plaCreateReport</b> or <b>plaRunRules</b>.


### -param Errors [out]

An <a href="https://msdn.microsoft.com/a7134395-91c6-4ea1-8b76-63830048289f">IValueMap</a> interface that you use to retrieve any errors that occurred. The value map can contain the list of directories where errors were encountered, along with the error codes. The <a href="https://msdn.microsoft.com/990b48d8-357f-4157-a3d2-1ea1c80e1887">IValueMap::Count</a> property is zero if there were no errors.


## -returns



Returns S_OK if successful.




## -remarks



Data management runs in the current process and blocks until the data management steps complete.

To automatically run the data manager when the data collector set finishes running, set the <a href="https://msdn.microsoft.com/3048a4b6-3e18-4585-bf5e-d91a4c0adcfc">IDataManager::Enabled</a> property to VARIANT_TRUE.




## -see-also




<a href="https://msdn.microsoft.com/a153d88f-4c7e-45fd-9cd8-497160711de4">IDataManager</a>
 

 

