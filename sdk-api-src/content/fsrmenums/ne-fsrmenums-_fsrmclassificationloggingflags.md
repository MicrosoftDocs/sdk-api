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
 

 

