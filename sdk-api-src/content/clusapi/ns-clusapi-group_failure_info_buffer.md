---
UID: NS:clusapi.GROUP_FAILURE_INFO_BUFFER
title: GROUP_FAILURE_INFO_BUFFER (clusapi.h)
description: The GROUP_FAILURE_INFO_BUFFER (clusapi.h) structure represents a buffer for a GROUP_FAILURE_INFO structure.
helpviewer_keywords: ["*PGROUP_FAILURE_INFO_BUFFER","GROUP_FAILURE_INFO_BUFFER","GROUP_FAILURE_INFO_BUFFER structure [Failover Cluster]","PGROUP_FAILURE_INFO_BUFFER","PGROUP_FAILURE_INFO_BUFFER structure pointer [Failover Cluster]","clusapi/GROUP_FAILURE_INFO_BUFFER","clusapi/PGROUP_FAILURE_INFO_BUFFER","msclus/GROUP_FAILURE_INFO_BUFFER","msclus/PGROUP_FAILURE_INFO_BUFFER","mscs.group_failure_info_buffer"]
old-location: mscs\group_failure_info_buffer.htm
tech.root: MsCS
ms.assetid: 69824D88-B9CE-451B-B65A-84822755CEAC
ms.date: 08/03/2022
ms.keywords: '*PGROUP_FAILURE_INFO_BUFFER, GROUP_FAILURE_INFO_BUFFER, GROUP_FAILURE_INFO_BUFFER structure [Failover Cluster], PGROUP_FAILURE_INFO_BUFFER, PGROUP_FAILURE_INFO_BUFFER structure pointer [Failover Cluster], clusapi/GROUP_FAILURE_INFO_BUFFER, clusapi/PGROUP_FAILURE_INFO_BUFFER, msclus/GROUP_FAILURE_INFO_BUFFER, msclus/PGROUP_FAILURE_INFO_BUFFER, mscs.group_failure_info_buffer'
req.header: clusapi.h
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
req.typenames: GROUP_FAILURE_INFO_BUFFER, *PGROUP_FAILURE_INFO_BUFFER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GROUP_FAILURE_INFO_BUFFER
 - clusapi/GROUP_FAILURE_INFO_BUFFER
 - PGROUP_FAILURE_INFO_BUFFER
 - clusapi/PGROUP_FAILURE_INFO_BUFFER
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
 - GROUP_FAILURE_INFO_BUFFER
---

# GROUP_FAILURE_INFO_BUFFER structure


## -description

Represents a buffer for a <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-group_failure_info">GROUP_FAILURE_INFO</a> structure.

## -struct-fields

### -field dwVersion

The version of this structure. Set this parameter to <b>GROUP_FAILURE_INFO_VERSION_1</b>        (0x1).

### -field Info

The <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-group_failure_info">GROUP_FAILURE_INFO</a> structure that contains information about the failover attempts for the group failure.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/utility-structures">Utility structures</a>
