---
UID: NE:fsrmenums._FsrmClassificationLoggingFlags
title: "_FsrmClassificationLoggingFlags"
author: windows-sdk-content
description: Defines the different options for logging information while running classification.
old-location: fsrm\fsrmclassificationloggingflags.htm
tech.root: Fsrm
ms.assetid: 339a50d6-cc34-46ba-a116-745abe0d2871
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: FsrmClassificationLoggingFlags, FsrmClassificationLoggingFlags enumeration [File Server Resource Manager], FsrmClassificationLoggingFlags_ClassificationsInLogFile, FsrmClassificationLoggingFlags_ClassificationsInSystemLog, FsrmClassificationLoggingFlags_ErrorsInLogFile, FsrmClassificationLoggingFlags_ErrorsInSystemLog, FsrmClassificationLoggingFlags_None, _FsrmClassificationLoggingFlags, fs.fsrmclassificationloggingflags, fsrm.fsrmclassificationloggingflags, fsrmenums/FsrmClassificationLoggingFlags, fsrmenums/FsrmClassificationLoggingFlags_ClassificationsInLogFile, fsrmenums/FsrmClassificationLoggingFlags_ClassificationsInSystemLog, fsrmenums/FsrmClassificationLoggingFlags_ErrorsInLogFile, fsrmenums/FsrmClassificationLoggingFlags_ErrorsInSystemLog, fsrmenums/FsrmClassificationLoggingFlags_None
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
 - FsrmClassificationLoggingFlags
product: Windows
targetos: Windows
req.typenames: FsrmClassificationLoggingFlags
req.redist: 
---

# _FsrmClassificationLoggingFlags enumeration


## -description


Defines the different options for logging information while running classification.


## -enum-fields




### -field FsrmClassificationLoggingFlags_None

No logging occurs.


### -field FsrmClassificationLoggingFlags_ClassificationsInLogFile

Logs to a log file information about all the files and properties that were classified.


### -field FsrmClassificationLoggingFlags_ErrorsInLogFile

Logs to a log file errors that occurred during classification.


### -field FsrmClassificationLoggingFlags_ClassificationsInSystemLog

Logs to the System event information about all the files and properties that were classified.


### -field FsrmClassificationLoggingFlags_ErrorsInSystemLog

Logs to the System event log errors that occurred during classification.


## -see-also




<a href="https://msdn.microsoft.com/c22f646b-36dc-45b8-a9ad-81ce6adab5bf">IFsrmClassificationManager.Logging</a>
 

 

