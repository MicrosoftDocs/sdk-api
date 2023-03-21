---
UID: NS:msclus.RESOURCE_FAILURE_INFO_BUFFER
title: RESOURCE_FAILURE_INFO_BUFFER (msclus.h)
description: The RESOURCE_FAILURE_INFO_BUFFER structure represents a buffer for a resource failure. (RESOURCE_FAILURE_INFO_BUFFER)
helpviewer_keywords: ["*PRESOURCE_FAILURE_INFO_BUFFER","PRESOURCE_FAILURE_INFO_BUFFER","PRESOURCE_FAILURE_INFO_BUFFER structure pointer [Failover Cluster]","RESOURCE_FAILURE_INFO_BUFFER","RESOURCE_FAILURE_INFO_BUFFER structure [Failover Cluster]","clusapi/PRESOURCE_FAILURE_INFO_BUFFER","clusapi/RESOURCE_FAILURE_INFO_BUFFER","msclus/PRESOURCE_FAILURE_INFO_BUFFER","msclus/RESOURCE_FAILURE_INFO_BUFFER","mscs.resource_failure_info_buffer"]
old-location: mscs\resource_failure_info_buffer.htm
tech.root: MsCS
ms.assetid: 131EEF4A-DB1E-4FF7-8329-4AA422AB83B0
ms.date: 08/02/2022
ms.keywords: '*PRESOURCE_FAILURE_INFO_BUFFER, PRESOURCE_FAILURE_INFO_BUFFER, PRESOURCE_FAILURE_INFO_BUFFER structure pointer [Failover Cluster], RESOURCE_FAILURE_INFO_BUFFER, RESOURCE_FAILURE_INFO_BUFFER structure [Failover Cluster], clusapi/PRESOURCE_FAILURE_INFO_BUFFER, clusapi/RESOURCE_FAILURE_INFO_BUFFER, msclus/PRESOURCE_FAILURE_INFO_BUFFER, msclus/RESOURCE_FAILURE_INFO_BUFFER, mscs.resource_failure_info_buffer'
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
req.typenames: RESOURCE_FAILURE_INFO_BUFFER, *PRESOURCE_FAILURE_INFO_BUFFER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RESOURCE_FAILURE_INFO_BUFFER
 - msclus/RESOURCE_FAILURE_INFO_BUFFER
 - PRESOURCE_FAILURE_INFO_BUFFER
 - msclus/PRESOURCE_FAILURE_INFO_BUFFER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusApi.h
 - MSClus.h
api_name:
 - RESOURCE_FAILURE_INFO_BUFFER
---

# RESOURCE_FAILURE_INFO_BUFFER structure


## -description

Represents a buffer for a resource failure.

## -struct-fields

### -field dwVersion

The version of this structure. Set this parameter to <b>RESOURCE_FAILURE_INFO_VERSION_1</b> (0x1).

### -field Info

The <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-resource_failure_info">RESOURCE_FAILURE_INFO</a> structure that contains information about the failover attempts for the resource failure.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/utility-structures">Utility structures</a>
