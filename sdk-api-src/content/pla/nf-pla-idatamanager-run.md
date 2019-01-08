---
UID: NF:pla.IDataManager.Run
title: IDataManager::Run
author: windows-sdk-content
description: Manually runs the data manager.
old-location: pla\idatamanager_run.htm
tech.root: PLA
ms.assetid: a1016784-8841-485f-885e-3719bdb0ae05
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDataManager interface [PLA],Run method, IDataManager.Run, IDataManager::Run, Run, Run method [PLA], Run method [PLA],IDataManager interface, base.idatamanager_run, pla.idatamanager_run, pla/IDataManager::Run
ms.topic: method
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Pla.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IDataManager.Run
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

