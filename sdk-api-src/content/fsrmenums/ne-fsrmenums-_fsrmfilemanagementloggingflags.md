---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

