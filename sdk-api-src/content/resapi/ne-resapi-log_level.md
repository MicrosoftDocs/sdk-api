---
UID: NE:resapi.LOG_LEVEL
title: LOG_LEVEL (resapi.h)
description: Represents the severity of the log event passed to the LogEvent callback function.
helpviewer_keywords: ["*PLOG_LEVEL","LOG_ERROR","LOG_INFORMATION","LOG_LEVEL","LOG_LEVEL enumeration [Failover Cluster]","LOG_SEVERE","LOG_WARNING","PLOG_LEVEL","PLOG_LEVEL enumeration pointer [Failover Cluster]","mscs.log_level","resapi/LOG_ERROR","resapi/LOG_INFORMATION","resapi/LOG_LEVEL","resapi/LOG_SEVERE","resapi/LOG_WARNING","resapi/PLOG_LEVEL"]
old-location: mscs\log_level.htm
tech.root: MsCS
ms.assetid: 976251d5-6619-47f7-9b6e-2031768100b0
ms.date: 12/05/2018
ms.keywords: '*PLOG_LEVEL, LOG_ERROR, LOG_INFORMATION, LOG_LEVEL, LOG_LEVEL enumeration [Failover Cluster], LOG_SEVERE, LOG_WARNING, PLOG_LEVEL, PLOG_LEVEL enumeration pointer [Failover Cluster], mscs.log_level, resapi/LOG_ERROR, resapi/LOG_INFORMATION, resapi/LOG_LEVEL, resapi/LOG_SEVERE, resapi/LOG_WARNING, resapi/PLOG_LEVEL'
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
req.typenames: LOG_LEVEL, *PLOG_LEVEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LOG_LEVEL
 - resapi/LOG_LEVEL
 - PLOG_LEVEL
 - resapi/PLOG_LEVEL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ResApi.h
api_name:
 - LOG_LEVEL
---

# LOG_LEVEL enumeration


## -description

Represents the severity of the log event passed to the 
    <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-plog_event_routine">LogEvent</a> callback function.

## -enum-fields

### -field LOG_INFORMATION

The event is informational.

### -field LOG_WARNING

The event is reporting a failure that might have happened, but it is uncertain whether a failure really did 
      occur.

### -field LOG_ERROR

The event affects a single component, but other components are not affected and the integrity of the rest 
      of the <a href="/previous-versions/windows/desktop/mscs/nodes">node</a> is not compromised.

### -field LOG_SEVERE

The event is reporting a severe failure that affects multiple components, or the integrity of the entire 
      system is compromised or believed to be compromised.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-plog_event_routine">LogEvent</a>