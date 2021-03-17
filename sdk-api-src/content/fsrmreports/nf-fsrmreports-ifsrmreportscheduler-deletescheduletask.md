---
UID: NF:fsrmreports.IFsrmReportScheduler.DeleteScheduleTask
title: IFsrmReportScheduler::DeleteScheduleTask (fsrmreports.h)
description: Deletes a task that is used to trigger a report job.
helpviewer_keywords: ["DeleteScheduleTask","DeleteScheduleTask method [File Server Resource Manager]","DeleteScheduleTask method [File Server Resource Manager]","FsrmReportScheduler class","DeleteScheduleTask method [File Server Resource Manager]","IFsrmReportScheduler interface","FsrmReportScheduler class [File Server Resource Manager]","DeleteScheduleTask method","IFsrmReportScheduler interface [File Server Resource Manager]","DeleteScheduleTask method","IFsrmReportScheduler.DeleteScheduleTask","IFsrmReportScheduler::DeleteScheduleTask","fs.ifsrmreportscheduler_deletescheduletask","fsrm.ifsrmreportscheduler_deletescheduletask","fsrmreports/IFsrmReportScheduler::DeleteScheduleTask"]
old-location: fsrm\ifsrmreportscheduler_deletescheduletask.htm
tech.root: fsrm
ms.assetid: 31541668-6173-48d4-8650-13e78bc7a763
ms.date: 12/05/2018
ms.keywords: DeleteScheduleTask, DeleteScheduleTask method [File Server Resource Manager], DeleteScheduleTask method [File Server Resource Manager],FsrmReportScheduler class, DeleteScheduleTask method [File Server Resource Manager],IFsrmReportScheduler interface, FsrmReportScheduler class [File Server Resource Manager],DeleteScheduleTask method, IFsrmReportScheduler interface [File Server Resource Manager],DeleteScheduleTask method, IFsrmReportScheduler.DeleteScheduleTask, IFsrmReportScheduler::DeleteScheduleTask, fs.ifsrmreportscheduler_deletescheduletask, fsrm.ifsrmreportscheduler_deletescheduletask, fsrmreports/IFsrmReportScheduler::DeleteScheduleTask
req.header: fsrmreports.h
req.include-header: FsrmReports.h, FsrmTlb.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmReports.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmReportScheduler::DeleteScheduleTask
 - fsrmreports/IFsrmReportScheduler::DeleteScheduleTask
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmReportScheduler.DeleteScheduleTask
 - FsrmReportScheduler.DeleteScheduleTask
---

# IFsrmReportScheduler::DeleteScheduleTask


## -description

<p class="CCE_Message">[Starting with Windows Server 2012 this method is not supported; use the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmscheduledtask">MSFT_FSRMScheduledTask</a> WMI class to manage 
    scheduled tasks.]

Deletes a task that is used to trigger a report job.

## -parameters

### -param taskName [in]

The name of a <a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a> 
      task to delete. The string is limited to 230 characters.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmreportscheduler">FsrmReportScheduler</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportscheduler">IFsrmReportScheduler</a>