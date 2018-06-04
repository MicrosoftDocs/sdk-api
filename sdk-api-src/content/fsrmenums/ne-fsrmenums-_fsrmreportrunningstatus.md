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

# _FsrmReportRunningStatus enumeration


## -description


Defines the running states a for a report job.


## -enum-fields




### -field FsrmReportRunningStatus_Unknown

The report job status in unknown.


### -field FsrmReportRunningStatus_NotRunning

The report job is not running.


### -field FsrmReportRunningStatus_Queued

The report job is queued to run but is not running.


### -field FsrmReportRunningStatus_Running

The report job is running.


## -see-also




<a href="https://msdn.microsoft.com/ae87183c-8e82-487c-b774-6b2b802fa645">IFsrmReportJob::RunningStatus</a>
 

 

