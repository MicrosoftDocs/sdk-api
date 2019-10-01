---
UID: NF:fsrmreports.IFsrmFileManagementJob.get_LastReportPathWithoutExtension
title: IFsrmFileManagementJob::get_LastReportPathWithoutExtension (fsrmreports.h)
author: windows-sdk-content
description: The local directory path where the reports were stored the last time the job ran.
old-location: fsrm\ifsrmfilemanagementjob_lastreportpathwithoutextension.htm
tech.root: fsrm
ms.assetid: 404d45e0-621e-47d5-b987-0f9347242653
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFsrmFileManagementJob interface [File Server Resource Manager],LastReportPathWithoutExtension property, IFsrmFileManagementJob.LastReportPathWithoutExtension, IFsrmFileManagementJob.get_LastReportPathWithoutExtension, IFsrmFileManagementJob::LastReportPathWithoutExtension, IFsrmFileManagementJob::get_LastReportPathWithoutExtension, LastReportPathWithoutExtension property [File Server Resource Manager], LastReportPathWithoutExtension property [File Server Resource Manager],IFsrmFileManagementJob interface, fs.ifsrmfilemanagementjob_lastreportpathwithoutextension, fsrm.ifsrmfilemanagementjob_lastreportpathwithoutextension, fsrmreports/IFsrmFileManagementJob::LastReportPathWithoutExtension, fsrmreports/IFsrmFileManagementJob::get_LastReportPathWithoutExtension, get_LastReportPathWithoutExtension
ms.topic: method
f1_keywords: 
 - "fsrmreports/IFsrmFileManagementJob.LastReportPathWithoutExtension"
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
 - IFsrmFileManagementJob.LastReportPathWithoutExtension
 - IFsrmFileManagementJob.get_LastReportPathWithoutExtension
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmFileManagementJob::get_LastReportPathWithoutExtension


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a> class.]

The local directory path where the reports were stored the last time the job ran.

This property is read-only.


## -parameters


## -remarks



If the job failed, this is the path where the reports would have been stored. The directory may contain 
    reports that completed successfully before the failure occurred.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmfilemanagementjob">IFsrmFileManagementJob</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a>
 

 

