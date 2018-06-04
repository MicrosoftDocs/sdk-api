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

# _CLFS_IOSTATS_CLASS enumeration


## -description


Defines types of I/O statistics reported by CLFS and is used when a client calls <a href="https://msdn.microsoft.com/1d4a5486-8a9e-480a-952c-12fc7386af3e">GetLogIoStatistics</a>.  Currently, log flush rates are the only type of statistic reported, but this enumeration will reflect more types of statistics in the future.


## -enum-fields




### -field ClfsIoStatsDefault

The default I/O statistics exported.


### -field ClfsIoStatsMax

The log flush rate.


## -see-also




<a href="https://msdn.microsoft.com/1d4a5486-8a9e-480a-952c-12fc7386af3e">GetLogIoStatistics</a>
 

 

