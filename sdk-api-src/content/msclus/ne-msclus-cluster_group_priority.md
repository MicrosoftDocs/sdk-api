---
UID: NE:msclus.CLUSTER_GROUP_PRIORITY
title: CLUSTER_GROUP_PRIORITY (msclus.h)
description: Specifies the priority level of a group.
helpviewer_keywords: ["CLUSTER_GROUP_PRIORITY","CLUSTER_GROUP_PRIORITY enumeration [Failover Cluster]","PriorityDisabled","PriorityHigh","PriorityLow","PriorityMedium","clusapi/CLUSTER_GROUP_PRIORITY","clusapi/PriorityDisabled","clusapi/PriorityHigh","clusapi/PriorityLow","clusapi/PriorityMedium","msclus/CLUSTER_GROUP_PRIORITY","msclus/PriorityDisabled","msclus/PriorityHigh","msclus/PriorityLow","msclus/PriorityMedium","mscs.cluster_group_priority"]
old-location: mscs\cluster_group_priority.htm
tech.root: MsCS
ms.assetid: CF2B9D74-72EC-4BBD-85C9-1BB0535580FB
ms.date: 12/05/2018
ms.keywords: CLUSTER_GROUP_PRIORITY, CLUSTER_GROUP_PRIORITY enumeration [Failover Cluster], PriorityDisabled, PriorityHigh, PriorityLow, PriorityMedium, clusapi/CLUSTER_GROUP_PRIORITY, clusapi/PriorityDisabled, clusapi/PriorityHigh, clusapi/PriorityLow, clusapi/PriorityMedium, msclus/CLUSTER_GROUP_PRIORITY, msclus/PriorityDisabled, msclus/PriorityHigh, msclus/PriorityLow, msclus/PriorityMedium, mscs.cluster_group_priority
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
req.typenames: CLUSTER_GROUP_PRIORITY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_GROUP_PRIORITY
 - msclus/CLUSTER_GROUP_PRIORITY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
 - MsClus.h
api_name:
 - CLUSTER_GROUP_PRIORITY
---

# CLUSTER_GROUP_PRIORITY enumeration


## -description

Specifies the priority level of a group.

## -enum-fields

### -field PriorityDisabled:0

Disabled priority. A group that has a disabled priority does not start automatically.

### -field PriorityLow:1000

Low priority.

### -field PriorityMedium:2000

Medium priority.

### -field PriorityHigh:3000

High priority.

