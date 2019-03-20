---
UID: NF:fsrmreports.IFsrmFileManagementJob.get_NamespaceRoots
title: IFsrmFileManagementJob::get_NamespaceRoots (fsrmreports.h)
author: windows-sdk-content
description: An array of local directory paths that will be scanned when the file management job is run.
old-location: fsrm\ifsrmfilemanagementjob_namespaceroots.htm
tech.root: fsrm
ms.assetid: 1f48ac40-eace-49f2-b77d-2456a1a5fa34
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFsrmFileManagementJob interface [File Server Resource Manager],NamespaceRoots property, IFsrmFileManagementJob.NamespaceRoots, IFsrmFileManagementJob.get_NamespaceRoots, IFsrmFileManagementJob::NamespaceRoots, IFsrmFileManagementJob::get_NamespaceRoots, IFsrmFileManagementJob::put_NamespaceRoots, NamespaceRoots property [File Server Resource Manager], NamespaceRoots property [File Server Resource Manager],IFsrmFileManagementJob interface, fs.ifsrmfilemanagementjob_namespaceroots, fsrm.ifsrmfilemanagementjob_namespaceroots, fsrmreports/IFsrmFileManagementJob::NamespaceRoots, fsrmreports/IFsrmFileManagementJob::get_NamespaceRoots, fsrmreports/IFsrmFileManagementJob::put_NamespaceRoots, get_NamespaceRoots
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmFileManagementJob::get_NamespaceRoots


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> class.]

An array of local directory paths that will be scanned when the file management job is 
    run.

This property is read/write.


## -parameters


## -remarks



All subdirectories under each specified path are also scanned (recursively).

If you schedule this job, specify the same namespaces when calling the 
    <a href="https://msdn.microsoft.com/983a6d05-417f-4aea-9652-955fd96e78f0">IFsrmReportScheduler::CreateScheduleTask</a> 
    method.

This property calls the 
    <a href="https://msdn.microsoft.com/bb5139c8-e01f-48cf-a8a9-d3a3e5b86238">IFsrmReportScheduler::VerifyNamespaces</a> 
    method to validate the paths. For validation details, see the Remarks section of 
    <b>VerifyNamespaces</b>.

Note that FSRM supports only NTFS file systems—you cannot specify paths on ReFS, FAT, 
    FAT32, UDF, or other non-NTFS file system.




## -see-also




<a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a>



<a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a>
 

 

