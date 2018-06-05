---
UID: NF:fsrmreports.IFsrmFileManagementJob.put_Logging
title: IFsrmFileManagementJob::put_Logging
author: windows-sdk-content
description: The types of logging to perform.
old-location: fsrm\ifsrmfilemanagementjob_logging.htm
old-project: Fsrm
ms.assetid: a1bed6bf-9c34-40ab-b5fc-ba870e1f084a
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: IFsrmFileManagementJob interface [File Server Resource Manager],Logging property, IFsrmFileManagementJob.Logging, IFsrmFileManagementJob.put_Logging, IFsrmFileManagementJob::Logging, IFsrmFileManagementJob::get_Logging, IFsrmFileManagementJob::put_Logging, Logging property [File Server Resource Manager], Logging property [File Server Resource Manager],IFsrmFileManagementJob interface, fs.ifsrmfilemanagementjob_logging, fsrm.ifsrmfilemanagementjob_logging, fsrmreports/IFsrmFileManagementJob::Logging, fsrmreports/IFsrmFileManagementJob::get_Logging, fsrmreports/IFsrmFileManagementJob::put_Logging, put_Logging
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FsrmTemplateApplyOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmFileManagementJob.Logging
-	IFsrmFileManagementJob.get_Logging
-	IFsrmFileManagementJob.put_Logging
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileManagementJob::put_Logging


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> class.]

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




<a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a>



<a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a>
 

 

