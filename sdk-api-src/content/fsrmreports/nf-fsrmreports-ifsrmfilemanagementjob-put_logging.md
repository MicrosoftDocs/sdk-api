---
UID: NF:fsrmreports.IFsrmFileManagementJob.put_Logging
title: IFsrmFileManagementJob::put_Logging (fsrmreports.h)
description: The types of logging to perform. (Put)
helpviewer_keywords: ["IFsrmFileManagementJob interface [File Server Resource Manager]","Logging property","IFsrmFileManagementJob.Logging","IFsrmFileManagementJob.put_Logging","IFsrmFileManagementJob::Logging","IFsrmFileManagementJob::get_Logging","IFsrmFileManagementJob::put_Logging","Logging property [File Server Resource Manager]","Logging property [File Server Resource Manager]","IFsrmFileManagementJob interface","fs.ifsrmfilemanagementjob_logging","fsrm.ifsrmfilemanagementjob_logging","fsrmreports/IFsrmFileManagementJob::Logging","fsrmreports/IFsrmFileManagementJob::get_Logging","fsrmreports/IFsrmFileManagementJob::put_Logging","put_Logging"]
old-location: fsrm\ifsrmfilemanagementjob_logging.htm
tech.root: fsrm
ms.assetid: a1bed6bf-9c34-40ab-b5fc-ba870e1f084a
ms.date: 12/05/2018
ms.keywords: IFsrmFileManagementJob interface [File Server Resource Manager],Logging property, IFsrmFileManagementJob.Logging, IFsrmFileManagementJob.put_Logging, IFsrmFileManagementJob::Logging, IFsrmFileManagementJob::get_Logging, IFsrmFileManagementJob::put_Logging, Logging property [File Server Resource Manager], Logging property [File Server Resource Manager],IFsrmFileManagementJob interface, fs.ifsrmfilemanagementjob_logging, fsrm.ifsrmfilemanagementjob_logging, fsrmreports/IFsrmFileManagementJob::Logging, fsrmreports/IFsrmFileManagementJob::get_Logging, fsrmreports/IFsrmFileManagementJob::put_Logging, put_Logging
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
 - IFsrmFileManagementJob::put_Logging
 - fsrmreports/IFsrmFileManagementJob::put_Logging
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
 - IFsrmFileManagementJob.Logging
 - IFsrmFileManagementJob.get_Logging
 - IFsrmFileManagementJob.put_Logging
---

# IFsrmFileManagementJob::put_Logging


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a> class.]

The types of logging to perform.

This property is read/write.

## -parameters

## -remarks

The log files are stored in the reports directory. The name of the 
    <b>FsrmFileManagementLoggingFlags_ClassificationsInLogFile</b> log file is 
    "FileManagement-<i>FsrmServerName(FQDN)</i>-<i>FileManagementJobName</i>-<i>NotificationPeriod</i>-<i>TimeStamp</i>.xml". 
    The log file contains one entry for each file processed. Each log entry specifies the following items:

<ul>
<li>File name (full path)</li>
<li>Owner</li>
<li>Command type</li>
<li>Command parameters</li>
<li>Error value</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmfilemanagementjob">IFsrmFileManagementJob</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a>
