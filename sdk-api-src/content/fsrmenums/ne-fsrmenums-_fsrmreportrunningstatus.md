---
UID: NE:fsrmenums._FsrmReportRunningStatus
title: "_FsrmReportRunningStatus"
author: windows-sdk-content
description: Defines the running states a for a report job.
old-location: fsrm\fsrmreportrunningstatus.htm
tech.root: Fsrm
ms.assetid: c14ba641-4f85-4a75-9d5c-d9381506c946
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: FsrmReportRunningStatus, FsrmReportRunningStatus enumeration [File Server Resource Manager], FsrmReportRunningStatus_NotRunning, FsrmReportRunningStatus_Queued, FsrmReportRunningStatus_Running, FsrmReportRunningStatus_Unknown, _FsrmReportRunningStatus, fs.fsrmreportrunningstatus, fsrm.fsrmreportrunningstatus, fsrmenums/FsrmReportRunningStatus, fsrmenums/FsrmReportRunningStatus_NotRunning, fsrmenums/FsrmReportRunningStatus_Queued, fsrmenums/FsrmReportRunningStatus_Running, fsrmenums/FsrmReportRunningStatus_Unknown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmReportRunningStatus
product: Windows
targetos: Windows
req.typenames: FsrmReportRunningStatus
req.redist: 
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
 

 

