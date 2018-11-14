---
UID: NE:fsrmenums._FsrmFileManagementLoggingFlags
title: "_FsrmFileManagementLoggingFlags"
author: windows-sdk-content
description: Defines the options for logging when running a file management job.
old-location: fsrm\fsrmfilemanagementloggingflags.htm
tech.root: Fsrm
ms.assetid: 8e6e40cb-a513-492b-bf2c-97238eb1d1db
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FsrmFileManagementLoggingFlags, FsrmFileManagementLoggingFlags enumeration [File Server Resource Manager], FsrmFileManagementLoggingFlags_Audit, FsrmFileManagementLoggingFlags_Error, FsrmFileManagementLoggingFlags_Information, FsrmFileManagementLoggingFlags_None, _FsrmFileManagementLoggingFlags, fs.fsrmfilemanagementloggingflags, fsrm.fsrmfilemanagementloggingflags, fsrmenums/FsrmFileManagementLoggingFlags, fsrmenums/FsrmFileManagementLoggingFlags_Audit, fsrmenums/FsrmFileManagementLoggingFlags_Error, fsrmenums/FsrmFileManagementLoggingFlags_Information, fsrmenums/FsrmFileManagementLoggingFlags_None
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
product: Windows
targetos: Windows
req.typenames: FsrmFileManagementLoggingFlags
req.redist: 
---

# _FsrmFileManagementLoggingFlags enumeration


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




<a href="https://msdn.microsoft.com/a1bed6bf-9c34-40ab-b5fc-ba870e1f084a">IFsrmFileManagementJob.Logging</a>
 

 

