---
UID: NE:isysmon.eDataSourceTypeConstant
title: DataSourceTypeConstants (isysmon.h)
description: Determines the source of the performance counter data.
helpviewer_keywords: ["DataSourceTypeConstants","DataSourceTypeConstants enumeration [SysMon]","base.datasourcetypeconstants","isysmon/DataSourceTypeConstants","isysmon/sysmonCurrentActivity","isysmon/sysmonLogFiles","isysmon/sysmonNullDataSource","isysmon/sysmonSqlLog","sysmon.datasourcetypeconstants","sysmonCurrentActivity","sysmonLogFiles","sysmonNullDataSource","sysmonSqlLog"]
old-location: sysmon\datasourcetypeconstants.htm
tech.root: SysMon
ms.assetid: ea281ef6-a9bc-4e4f-bd05-642a9c48de73
ms.date: 12/05/2018
ms.keywords: DataSourceTypeConstants, DataSourceTypeConstants enumeration [SysMon], base.datasourcetypeconstants, isysmon/DataSourceTypeConstants, isysmon/sysmonCurrentActivity, isysmon/sysmonLogFiles, isysmon/sysmonNullDataSource, isysmon/sysmonSqlLog, sysmon.datasourcetypeconstants, sysmonCurrentActivity, sysmonLogFiles, sysmonNullDataSource, sysmonSqlLog
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DataSourceTypeConstants
req.redist: 
ms.custom: 19H1
f1_keywords:
 - eDataSourceTypeConstant
 - isysmon/eDataSourceTypeConstant
 - DataSourceTypeConstants
 - isysmon/DataSourceTypeConstants
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ISysmon.h
api_name:
 - DataSourceTypeConstants
---

# DataSourceTypeConstants enumeration


## -description

Determines the source of the performance counter data.

## -enum-fields

### -field sysmonNullDataSource:0xffffffff

No data source.

### -field sysmonCurrentActivity:0x1

The data source is the current activity of the performance counters on the local or remote computer as specified in the performance counter paths.

### -field sysmonLogFiles:0x2

The data source is one or more log files.

### -field sysmonSqlLog:0x3

The data source is an SQL log.

## -see-also

<a href="/windows/desktop/SysMon/systemmonitor-datasourcetype">SystemMonitor.DataSourceType</a>
