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

# eDataSourceTypeConstant enumeration


## -description


Determines the source of the performance counter data.


## -enum-fields




### -field sysmonNullDataSource

No data source.


### -field sysmonCurrentActivity

The data source is the current activity of the performance counters on the local or remote computer as specified in the performance counter paths. 


### -field sysmonLogFiles

The data source is one or more log files.


### -field sysmonSqlLog

The data source is an SQL log.


## -see-also




<a href="https://msdn.microsoft.com/53c1e9bc-dafd-445c-8d82-13a74f6c488a">SystemMonitor.DataSourceType</a>
 

 

