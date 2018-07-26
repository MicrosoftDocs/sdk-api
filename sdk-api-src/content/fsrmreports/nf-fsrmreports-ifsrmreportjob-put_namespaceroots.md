---
UID: NF:fsrmreports.IFsrmReportJob.put_NamespaceRoots
title: IFsrmReportJob::put_NamespaceRoots
author: windows-sdk-content
description: Retrieves or sets an array of local directory paths that will be scanned when the report job is run.
old-location: fsrm\ifsrmreportjob_namespaceroots.htm
old-project: Fsrm
ms.assetid: 09c767ce-6a81-4c06-93cb-dd1a79d17d97
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IFsrmReportJob interface [File Server Resource Manager],NamespaceRoots property, IFsrmReportJob.NamespaceRoots, IFsrmReportJob.put_NamespaceRoots, IFsrmReportJob::NamespaceRoots, IFsrmReportJob::get_NamespaceRoots, IFsrmReportJob::put_NamespaceRoots, NamespaceRoots property [File Server Resource Manager], NamespaceRoots property [File Server Resource Manager],IFsrmReportJob interface, fs.ifsrmreportjob_namespaceroots, fsrm.ifsrmreportjob_namespaceroots, fsrmreports/IFsrmReportJob::NamespaceRoots, fsrmreports/IFsrmReportJob::get_NamespaceRoots, fsrmreports/IFsrmReportJob::put_NamespaceRoots, put_NamespaceRoots
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: FsrmTemplateApplyOptions
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
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmReportJob::put_NamespaceRoots


## -description


Retrieves or sets an array of local directory paths that will be scanned when the report job is 
    run.

This property is read/write.


## -parameters


## -remarks



All subdirectories under the specified path are also scanned (recursively).

If you schedule this job, specify the same namespaces when calling the 
    <a href="https://msdn.microsoft.com/983a6d05-417f-4aea-9652-955fd96e78f0">IFsrmReportScheduler::CreateScheduleTask</a> 
    method.

This property calls the 
    <a href="https://msdn.microsoft.com/bb5139c8-e01f-48cf-a8a9-d3a3e5b86238">IFsrmReportScheduler::VerifyNamespaces</a> 
    method to validate the paths. For validation details, see the Remarks section of 
    <b>VerifyNamespaces</b>.

Note that FSRM supports only NTFS file systems—you cannot specify paths on ReFS, FAT, 
    FAT32, UDF, or other non-NTFS file system.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/a91c4fe7-ec8c-4d2b-b565-559e16668c87">Defining a Report Job</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/ea8a3f6b-326b-4c8f-a6fc-7b7525c5543f">IFsrmReportJob</a>
 

 

