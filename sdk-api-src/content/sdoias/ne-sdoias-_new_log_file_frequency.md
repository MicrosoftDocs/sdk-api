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

# _NEW_LOG_FILE_FREQUENCY enumeration


## -description


The values of the 
<b>NEW_LOG_FILE_FREQUENCY</b> enumeration type specify how frequently new log files are created.


## -enum-fields




### -field IAS_LOGGING_UNLIMITED_SIZE

Allows the log file to grow without limit. Do not create new log files periodically.


### -field IAS_LOGGING_DAILY

Creates a new log file each day.


### -field IAS_LOGGING_WEEKLY

Creates a new log file each week.


### -field IAS_LOGGING_MONTHLY

Creates a new log file each month.


### -field IAS_LOGGING_WHEN_FILE_SIZE_REACHES

Creates a new log file when the log file reaches a particular size.


## -see-also




<a href="https://msdn.microsoft.com/e814d576-0405-410e-ae62-e0f5905f6cf9">ACCOUNTINGPROPERTIES</a>
 

 

