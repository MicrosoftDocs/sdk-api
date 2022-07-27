---
UID: NF:fsrmreports.IFsrmReportJob.get_Task
title: IFsrmReportJob::get_Task (fsrmreports.h)
description: Retrieves or sets the name of the report job. (Get)
helpviewer_keywords: ["IFsrmReportJob interface [File Server Resource Manager]","Task property","IFsrmReportJob.Task","IFsrmReportJob.get_Task","IFsrmReportJob::Task","IFsrmReportJob::get_Task","IFsrmReportJob::put_Task","Task property [File Server Resource Manager]","Task property [File Server Resource Manager]","IFsrmReportJob interface","fs.ifsrmreportjob_task","fsrm.ifsrmreportjob_task","fsrmreports/IFsrmReportJob::Task","fsrmreports/IFsrmReportJob::get_Task","fsrmreports/IFsrmReportJob::put_Task","get_Task"]
old-location: fsrm\ifsrmreportjob_task.htm
tech.root: fsrm
ms.assetid: 2c9ceaca-f696-4506-bc25-efd601522560
ms.date: 12/05/2018
ms.keywords: IFsrmReportJob interface [File Server Resource Manager],Task property, IFsrmReportJob.Task, IFsrmReportJob.get_Task, IFsrmReportJob::Task, IFsrmReportJob::get_Task, IFsrmReportJob::put_Task, Task property [File Server Resource Manager], Task property [File Server Resource Manager],IFsrmReportJob interface, fs.ifsrmreportjob_task, fsrm.ifsrmreportjob_task, fsrmreports/IFsrmReportJob::Task, fsrmreports/IFsrmReportJob::get_Task, fsrmreports/IFsrmReportJob::put_Task, get_Task
req.header: fsrmreports.h
req.include-header: 
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
req.dll: SrmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmReportJob::get_Task
 - fsrmreports/IFsrmReportJob::get_Task
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
 - IFsrmReportJob.Task
 - IFsrmReportJob.get_Task
 - IFsrmReportJob.put_Task
---

# IFsrmReportJob::get_Task


## -description

Retrieves or sets the name of the report job.

This property is read/write.

## -parameters

## -remarks

Typically, the name is the same name that you specify when you call the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportscheduler-createscheduletask">IFsrmReportScheduler::CreateScheduleTask</a> 
    method to create a scheduled task that runs the report job.

Use the task name when calling the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-getreportjob">IFsrmReportManager::GetReportJob</a> method to 
    retrieve a report job.


#### Examples

For an example, see <a href="/previous-versions/windows/desktop/fsrm/defining-a-report-job">Defining a Report Job</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportjob">IFsrmReportJob</a>
