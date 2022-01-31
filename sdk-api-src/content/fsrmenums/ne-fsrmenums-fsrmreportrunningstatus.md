---
UID: NE:fsrmenums._FsrmReportRunningStatus
title: FsrmReportRunningStatus (fsrmenums.h)
description: Defines the running states a for a report job.
helpviewer_keywords: ["FsrmReportRunningStatus","FsrmReportRunningStatus enumeration [File Server Resource Manager]","FsrmReportRunningStatus_NotRunning","FsrmReportRunningStatus_Queued","FsrmReportRunningStatus_Running","FsrmReportRunningStatus_Unknown","fs.fsrmreportrunningstatus","fsrm.fsrmreportrunningstatus","fsrmenums/FsrmReportRunningStatus","fsrmenums/FsrmReportRunningStatus_NotRunning","fsrmenums/FsrmReportRunningStatus_Queued","fsrmenums/FsrmReportRunningStatus_Running","fsrmenums/FsrmReportRunningStatus_Unknown"]
old-location: fsrm\fsrmreportrunningstatus.htm
tech.root: fsrm
ms.assetid: c14ba641-4f85-4a75-9d5c-d9381506c946
ms.date: 12/05/2018
ms.keywords: FsrmReportRunningStatus, FsrmReportRunningStatus enumeration [File Server Resource Manager], FsrmReportRunningStatus_NotRunning, FsrmReportRunningStatus_Queued, FsrmReportRunningStatus_Running, FsrmReportRunningStatus_Unknown, fs.fsrmreportrunningstatus, fsrm.fsrmreportrunningstatus, fsrmenums/FsrmReportRunningStatus, fsrmenums/FsrmReportRunningStatus_NotRunning, fsrmenums/FsrmReportRunningStatus_Queued, fsrmenums/FsrmReportRunningStatus_Running, fsrmenums/FsrmReportRunningStatus_Unknown
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
targetos: Windows
req.typenames: FsrmReportRunningStatus
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FsrmReportRunningStatus
 - fsrmenums/_FsrmReportRunningStatus
 - FsrmReportRunningStatus
 - fsrmenums/FsrmReportRunningStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmReportRunningStatus
---

# FsrmReportRunningStatus enumeration


## -description

Defines the running states a for a report job.

## -enum-fields

### -field FsrmReportRunningStatus_Unknown:0

The report job status in unknown.

### -field FsrmReportRunningStatus_NotRunning:1

The report job is not running.

### -field FsrmReportRunningStatus_Queued:2

The report job is queued to run but is not running.

### -field FsrmReportRunningStatus_Running:3

The report job is running.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-get_runningstatus">IFsrmReportJob::RunningStatus</a>
