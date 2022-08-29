---
UID: NS:msclus.RESOURCE_FAILURE_INFO
title: RESOURCE_FAILURE_INFO (msclus.h)
description: The RESOURCE_FAILURE_INFO structure represents information about the Failover attempts for a resource and is used by the RESOURCE_FAILURE_INFO_BUFFER structure. 
helpviewer_keywords: ["*PRESOURCE_FAILURE_INFO","PRESOURCE_FAILURE_INFO","PRESOURCE_FAILURE_INFO structure pointer [Failover Cluster]","RESOURCE_FAILURE_INFO","RESOURCE_FAILURE_INFO structure [Failover Cluster]","clusapi/PRESOURCE_FAILURE_INFO","clusapi/RESOURCE_FAILURE_INFO","msclus/PRESOURCE_FAILURE_INFO","msclus/RESOURCE_FAILURE_INFO","mscs.resource_failure_info"]
old-location: mscs\resource_failure_info.htm
tech.root: MsCS
ms.assetid: 3FE0CC0E-B097-48FC-882F-F6B236BB0CCB
ms.date: 08/02/2022
ms.keywords: '*PRESOURCE_FAILURE_INFO, PRESOURCE_FAILURE_INFO, PRESOURCE_FAILURE_INFO structure pointer [Failover Cluster], RESOURCE_FAILURE_INFO, RESOURCE_FAILURE_INFO structure [Failover Cluster], clusapi/PRESOURCE_FAILURE_INFO, clusapi/RESOURCE_FAILURE_INFO, msclus/PRESOURCE_FAILURE_INFO, msclus/RESOURCE_FAILURE_INFO, mscs.resource_failure_info'
req.header: msclus.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
req.typenames: RESOURCE_FAILURE_INFO, *PRESOURCE_FAILURE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RESOURCE_FAILURE_INFO
 - msclus/RESOURCE_FAILURE_INFO
 - PRESOURCE_FAILURE_INFO
 - msclus/PRESOURCE_FAILURE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusApi.h
 - MsClus.h
api_name:
 - RESOURCE_FAILURE_INFO
---

# RESOURCE_FAILURE_INFO structure


## -description

Represents information about the <a href="/previous-versions/windows/desktop/mscs/failover">Failover</a> attempts for a resource. This structure is used by the <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-resource_failure_info_buffer">RESOURCE_FAILURE_INFO_BUFFER</a> structure.

## -struct-fields

### -field dwRestartAttemptsRemaining

The number of remaining failover attempts that can be made on the resource during the current <a href="/previous-versions/windows/desktop/mscs/groups-failoverperiod">FailoverPeriod</a> time interval.

### -field dwRestartPeriodRemaining

The amount of time remaining for the <a href="/previous-versions/windows/desktop/mscs/groups-failoverperiod">FailoverPeriod</a>, in seconds.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-resource_failure_info_buffer">RESOURCE_FAILURE_INFO_BUFFER</a>



<a href="/previous-versions/windows/desktop/mscs/utility-structures">Utility Structures</a>
