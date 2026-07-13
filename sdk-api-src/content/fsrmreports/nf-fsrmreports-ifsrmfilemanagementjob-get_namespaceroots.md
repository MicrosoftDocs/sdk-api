---
UID: NF:fsrmreports.IFsrmFileManagementJob.get_NamespaceRoots
title: IFsrmFileManagementJob::get_NamespaceRoots (fsrmreports.h)
description: An array of local directory paths that will be scanned when the file management job is run. (Get)
helpviewer_keywords: ["IFsrmFileManagementJob interface [File Server Resource Manager]","NamespaceRoots property","IFsrmFileManagementJob.NamespaceRoots","IFsrmFileManagementJob.get_NamespaceRoots","IFsrmFileManagementJob::NamespaceRoots","IFsrmFileManagementJob::get_NamespaceRoots","IFsrmFileManagementJob::put_NamespaceRoots","NamespaceRoots property [File Server Resource Manager]","NamespaceRoots property [File Server Resource Manager]","IFsrmFileManagementJob interface","fs.ifsrmfilemanagementjob_namespaceroots","fsrm.ifsrmfilemanagementjob_namespaceroots","fsrmreports/IFsrmFileManagementJob::NamespaceRoots","fsrmreports/IFsrmFileManagementJob::get_NamespaceRoots","fsrmreports/IFsrmFileManagementJob::put_NamespaceRoots","get_NamespaceRoots"]
old-location: fsrm\ifsrmfilemanagementjob_namespaceroots.htm
tech.root: fsrm
ms.assetid: 1f48ac40-eace-49f2-b77d-2456a1a5fa34
ms.date: 12/05/2018
ms.keywords: IFsrmFileManagementJob interface [File Server Resource Manager],NamespaceRoots property, IFsrmFileManagementJob.NamespaceRoots, IFsrmFileManagementJob.get_NamespaceRoots, IFsrmFileManagementJob::NamespaceRoots, IFsrmFileManagementJob::get_NamespaceRoots, IFsrmFileManagementJob::put_NamespaceRoots, NamespaceRoots property [File Server Resource Manager], NamespaceRoots property [File Server Resource Manager],IFsrmFileManagementJob interface, fs.ifsrmfilemanagementjob_namespaceroots, fsrm.ifsrmfilemanagementjob_namespaceroots, fsrmreports/IFsrmFileManagementJob::NamespaceRoots, fsrmreports/IFsrmFileManagementJob::get_NamespaceRoots, fsrmreports/IFsrmFileManagementJob::put_NamespaceRoots, get_NamespaceRoots
req.header: fsrmreports.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
 - IFsrmFileManagementJob::get_NamespaceRoots
 - fsrmreports/IFsrmFileManagementJob::get_NamespaceRoots
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
 - IFsrmFileManagementJob.NamespaceRoots
 - IFsrmFileManagementJob.get_NamespaceRoots
 - IFsrmFileManagementJob.put_NamespaceRoots
---

# IFsrmFileManagementJob::get_NamespaceRoots


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a> class.]

An array of local directory paths that will be scanned when the file management job is 
    run.

This property is read/write.

## -parameters

## -remarks

All subdirectories under each specified path are also scanned (recursively).

If you schedule this job, specify the same namespaces when calling the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportscheduler-createscheduletask">IFsrmReportScheduler::CreateScheduleTask</a> 
    method.

This property calls the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportscheduler-verifynamespaces">IFsrmReportScheduler::VerifyNamespaces</a> 
    method to validate the paths. For validation details, see the Remarks section of 
    <b>VerifyNamespaces</b>.

Note that FSRM supports only NTFS file systems—you cannot specify paths on ReFS, FAT, 
    FAT32, UDF, or other non-NTFS file system.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmfilemanagementjob">IFsrmFileManagementJob</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a>
