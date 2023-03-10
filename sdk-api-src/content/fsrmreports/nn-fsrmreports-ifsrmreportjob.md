---
UID: NN:fsrmreports.IFsrmReportJob
title: IFsrmReportJob (fsrmreports.h)
description: Used to configure a report job.
helpviewer_keywords: ["IFsrmReportJob","IFsrmReportJob interface [File Server Resource Manager]","IFsrmReportJob interface [File Server Resource Manager]","described","fs.ifsrmreportjob","fsrm.ifsrmreportjob","fsrm/IFsrmReportJob"]
old-location: fsrm\ifsrmreportjob.htm
tech.root: fsrm
ms.assetid: ea8a3f6b-326b-4c8f-a6fc-7b7525c5543f
ms.date: 12/05/2018
ms.keywords: IFsrmReportJob, IFsrmReportJob interface [File Server Resource Manager], IFsrmReportJob interface [File Server Resource Manager],described, fs.ifsrmreportjob, fsrm.ifsrmreportjob, fsrm/IFsrmReportJob
req.header: fsrmreports.h
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
req.dll: SrmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmReportJob
 - fsrmreports/IFsrmReportJob
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
 - IFsrmReportJob
---

# IFsrmReportJob interface


## -description

Used to configure a report job. The job specifies a set of directories that will be scanned 
    to generate one or more different type of reports. The reports help the administrator analyze how the storage is 
    used. The job may also be associated with a scheduled task that will trigger report generation.

To create this interface, call the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-createreportjob">IFsrmReportManager::CreateReportJob</a> 
    method.

The following methods return this interface:
<ul>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-enumreportjobs">IFsrmReportManager::EnumReportJobs</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-getreportjob">IFsrmReportManager::GetReportJob</a>
</li>
</ul>

## -inheritance

The <b>IFsrmReportJob</b> interface inherits from <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmobject">IFsrmObject</a>. <b>IFsrmReportJob</b> also has these types of members:

## -remarks

To <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-commit">commit</a> the job, you must specify at least one 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-createreport">report type</a>, at least one 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-get_namespaceroots">namespace root</a>, and the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-get_task">task name</a>.

To <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-run">run</a> the job, you must specify at least one 
   <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-createreport">report type</a> and 
   <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-get_namespaceroots">namespace root</a>.
