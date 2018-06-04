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

# IMFWorkQueueServicesEx::BeginRegisterPlatformWorkQueueWithMMCSSEx


## -description


Registers a platform work queue with Multimedia Class Scheduler Service (MMCSS) using the specified
    class and task id.


## -parameters




### -param dwPlatformWorkQueue [in]

The id of one of the standard platform work queues.


### -param wszClass [in]

The MMCSS class which the work queue should be registered with.


### -param dwTaskId [in]

    The task id which the work queue should be registered with. If <i>dwTaskId</i> is 0, a new MMCSS bucket will be created.


### -param lPriority [in]

The priority.


### -param pCallback [in]

Standard callback used for async operations in Media Foundation.


### -param pState [in]

Standard state used for async operations in Media Foundation.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/12d4f0f4-9a6d-4782-b5ae-4add6608782a">IMFWorkQueueServicesEx</a>
 

 

