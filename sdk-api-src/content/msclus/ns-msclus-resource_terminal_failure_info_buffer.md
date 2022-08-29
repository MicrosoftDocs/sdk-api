---
UID: NS:msclus.RESOURCE_TERMINAL_FAILURE_INFO_BUFFER
title: RESOURCE_TERMINAL_FAILURE_INFO_BUFFER (msclus.h)
description: The RESOURCE_TERMINAL_FAILURE_INFO_BUFFER structure represents a buffer for a terminal failure for a resource.
helpviewer_keywords: ["*PRESOURCE_TERMINAL_FAILURE_INFO_BUFFER","PRESOURCE_TERMINAL_FAILURE_INFO_BUFFER","PRESOURCE_TERMINAL_FAILURE_INFO_BUFFER structure pointer [Failover Cluster]","RESOURCE_TERMINAL_FAILURE_INFO_BUFFER","RESOURCE_TERMINAL_FAILURE_INFO_BUFFER structure [Failover Cluster]","clusapi/PRESOURCE_TERMINAL_FAILURE_INFO_BUFFER","clusapi/RESOURCE_TERMINAL_FAILURE_INFO_BUFFER","msclus/PRESOURCE_TERMINAL_FAILURE_INFO_BUFFER","msclus/RESOURCE_TERMINAL_FAILURE_INFO_BUFFER","mscs.resource_terminal_failure_info_buffer"]
old-location: mscs\resource_terminal_failure_info_buffer.htm
tech.root: MsCS
ms.assetid: D84EEF3A-BDB4-4D6E-BDC6-5A39DC32945E
ms.date: 08/02/2022
ms.keywords: '*PRESOURCE_TERMINAL_FAILURE_INFO_BUFFER, PRESOURCE_TERMINAL_FAILURE_INFO_BUFFER, PRESOURCE_TERMINAL_FAILURE_INFO_BUFFER structure pointer [Failover Cluster], RESOURCE_TERMINAL_FAILURE_INFO_BUFFER, RESOURCE_TERMINAL_FAILURE_INFO_BUFFER structure [Failover Cluster], clusapi/PRESOURCE_TERMINAL_FAILURE_INFO_BUFFER, clusapi/RESOURCE_TERMINAL_FAILURE_INFO_BUFFER, msclus/PRESOURCE_TERMINAL_FAILURE_INFO_BUFFER, msclus/RESOURCE_TERMINAL_FAILURE_INFO_BUFFER, mscs.resource_terminal_failure_info_buffer'
req.header: msclus.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 R2
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
req.typenames: RESOURCE_TERMINAL_FAILURE_INFO_BUFFER, *PRESOURCE_TERMINAL_FAILURE_INFO_BUFFER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RESOURCE_TERMINAL_FAILURE_INFO_BUFFER
 - msclus/RESOURCE_TERMINAL_FAILURE_INFO_BUFFER
 - PRESOURCE_TERMINAL_FAILURE_INFO_BUFFER
 - msclus/PRESOURCE_TERMINAL_FAILURE_INFO_BUFFER
dev_langs:
 - c++
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
api_name:
 - RESOURCE_TERMINAL_FAILURE_INFO_BUFFER
---

# RESOURCE_TERMINAL_FAILURE_INFO_BUFFER structure


## -description

Represents a buffer for a terminal failure for a resource.

## -struct-fields

### -field isTerminalFailure

<b>TRUE</b> if the resource  failure is a terminal failure; otherwise, <b>FALSE</b>.

### -field restartPeriodRemaining

The amount of time remaining for the TBD, in seconds.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/utility-structures">Utility structures</a>
