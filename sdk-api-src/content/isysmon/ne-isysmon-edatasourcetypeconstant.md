---
UID: NE:isysmon.eDataSourceTypeConstant
title: eDataSourceTypeConstant
author: windows-sdk-content
description: Determines the source of the performance counter data.
old-location: sysmon\datasourcetypeconstants.htm
old-project: sysmon
ms.assetid: ea281ef6-a9bc-4e4f-bd05-642a9c48de73
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DataSourceTypeConstants, DataSourceTypeConstants enumeration [SysMon], base.datasourcetypeconstants, eDataSourceTypeConstant, isysmon/DataSourceTypeConstants, isysmon/sysmonCurrentActivity, isysmon/sysmonLogFiles, isysmon/sysmonNullDataSource, isysmon/sysmonSqlLog, sysmon.datasourcetypeconstants, sysmonCurrentActivity, sysmonLogFiles, sysmonNullDataSource, sysmonSqlLog
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: isysmon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: DataSourceTypeConstants
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ISysmon.h
api_name:
 - DataSourceTypeConstants
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

