---
UID: NF:fsrmreports.IFsrmReportJob.get_NamespaceRoots
title: IFsrmReportJob::get_NamespaceRoots (fsrmreports.h)
description: Retrieves or sets an array of local directory paths that will be scanned when the report job is run. (Get)
helpviewer_keywords: ["IFsrmReportJob interface [File Server Resource Manager]","NamespaceRoots property","IFsrmReportJob.NamespaceRoots","IFsrmReportJob.get_NamespaceRoots","IFsrmReportJob::NamespaceRoots","IFsrmReportJob::get_NamespaceRoots","IFsrmReportJob::put_NamespaceRoots","NamespaceRoots property [File Server Resource Manager]","NamespaceRoots property [File Server Resource Manager]","IFsrmReportJob interface","fs.ifsrmreportjob_namespaceroots","fsrm.ifsrmreportjob_namespaceroots","fsrmreports/IFsrmReportJob::NamespaceRoots","fsrmreports/IFsrmReportJob::get_NamespaceRoots","fsrmreports/IFsrmReportJob::put_NamespaceRoots","get_NamespaceRoots"]
old-location: fsrm\ifsrmreportjob_namespaceroots.htm
tech.root: fsrm
ms.assetid: 09c767ce-6a81-4c06-93cb-dd1a79d17d97
ms.date: 12/05/2018
ms.keywords: IFsrmReportJob interface [File Server Resource Manager],NamespaceRoots property, IFsrmReportJob.NamespaceRoots, IFsrmReportJob.get_NamespaceRoots, IFsrmReportJob::NamespaceRoots, IFsrmReportJob::get_NamespaceRoots, IFsrmReportJob::put_NamespaceRoots, NamespaceRoots property [File Server Resource Manager], NamespaceRoots property [File Server Resource Manager],IFsrmReportJob interface, fs.ifsrmreportjob_namespaceroots, fsrm.ifsrmreportjob_namespaceroots, fsrmreports/IFsrmReportJob::NamespaceRoots, fsrmreports/IFsrmReportJob::get_NamespaceRoots, fsrmreports/IFsrmReportJob::put_NamespaceRoots, get_NamespaceRoots
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
 - IFsrmReportJob::get_NamespaceRoots
 - fsrmreports/IFsrmReportJob::get_NamespaceRoots
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
 - IFsrmReportJob.NamespaceRoots
 - IFsrmReportJob.get_NamespaceRoots
 - IFsrmReportJob.put_NamespaceRoots
---

# IFsrmReportJob::get_NamespaceRoots


## -description

Retrieves or sets an array of local directory paths that will be scanned when the report job is 
    run.

This property is read/write.

## -parameters

## -remarks

All subdirectories under the specified path are also scanned (recursively).

If you schedule this job, specify the same namespaces when calling the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportscheduler-createscheduletask">IFsrmReportScheduler::CreateScheduleTask</a> 
    method.

This property calls the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportscheduler-verifynamespaces">IFsrmReportScheduler::VerifyNamespaces</a> 
    method to validate the paths. For validation details, see the Remarks section of 
    <b>VerifyNamespaces</b>.

Note that FSRM supports only NTFS file systems—you cannot specify paths on ReFS, FAT, 
    FAT32, UDF, or other non-NTFS file system.


#### Examples

For an example, see <a href="/previous-versions/windows/desktop/fsrm/defining-a-report-job">Defining a Report Job</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportjob">IFsrmReportJob</a>
