---
UID: NE:fsrmenums._FsrmFileManagementLoggingFlags
title: FsrmFileManagementLoggingFlags (fsrmenums.h)
author: windows-sdk-content
description: Defines the options for logging when running a file management job.
old-location: fsrm\fsrmfilemanagementloggingflags.htm
tech.root: fsrm
ms.assetid: 8e6e40cb-a513-492b-bf2c-97238eb1d1db
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FsrmFileManagementLoggingFlags, FsrmFileManagementLoggingFlags enumeration [File Server Resource Manager], FsrmFileManagementLoggingFlags_Audit, FsrmFileManagementLoggingFlags_Error, FsrmFileManagementLoggingFlags_Information, FsrmFileManagementLoggingFlags_None, fs.fsrmfilemanagementloggingflags, fsrm.fsrmfilemanagementloggingflags, fsrmenums/FsrmFileManagementLoggingFlags, fsrmenums/FsrmFileManagementLoggingFlags_Audit, fsrmenums/FsrmFileManagementLoggingFlags_Error, fsrmenums/FsrmFileManagementLoggingFlags_Information, fsrmenums/FsrmFileManagementLoggingFlags_None
ms.topic: enum
f1_keywords: 
 - "fsrmenums/FsrmFileManagementLoggingFlags"
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmFileManagementLoggingFlags
targetos: Windows
req.typenames: FsrmFileManagementLoggingFlags
req.redist: 
ms.custom: 19H1
---

# FsrmFileManagementLoggingFlags enumeration


## -description


Defines the options for logging when running a file management job.


## -enum-fields




### -field FsrmFileManagementLoggingFlags_None

Do not log events.


### -field FsrmFileManagementLoggingFlags_Error

Log errors that occur when running the file management job to a log file.


### -field FsrmFileManagementLoggingFlags_Information

Log information status messages that occur when running the file management job to a log file.


### -field FsrmFileManagementLoggingFlags_Audit

Log information about every file that met all of the file management job's conditions to the Security audit 
      log.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_logging">IFsrmFileManagementJob.Logging</a>
 

 

