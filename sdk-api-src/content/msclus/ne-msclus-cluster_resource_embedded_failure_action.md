---
UID: NE:msclus.CLUSTER_RESOURCE_EMBEDDED_FAILURE_ACTION
title: CLUSTER_RESOURCE_EMBEDDED_FAILURE_ACTION (msclus.h)
description: Specifies the various actions that can be performed when a resource has an embedded failure.
helpviewer_keywords: ["CLUSTER_RESOURCE_EMBEDDED_FAILURE_ACTION","CLUSTER_RESOURCE_EMBEDDED_FAILURE_ACTION enumeration [Failover Cluster]","ClusterResourceEmbeddedFailureActionLogOnly","ClusterResourceEmbeddedFailureActionNone","ClusterResourceEmbeddedFailureActionRecover","clusapi/CLUSTER_RESOURCE_EMBEDDED_FAILURE_ACTION","clusapi/ClusterResourceEmbeddedFailureActionLogOnly","clusapi/ClusterResourceEmbeddedFailureActionNone","clusapi/ClusterResourceEmbeddedFailureActionRecover","msclus/CLUSTER_RESOURCE_EMBEDDED_FAILURE_ACTION","msclus/ClusterResourceEmbeddedFailureActionLogOnly","msclus/ClusterResourceEmbeddedFailureActionNone","msclus/ClusterResourceEmbeddedFailureActionRecover","mscs.cluster_resource_embedded_failure_action"]
old-location: mscs\cluster_resource_embedded_failure_action.htm
tech.root: MsCS
ms.assetid: 72251E97-0DBC-4EEA-BACF-3F7677483F29
ms.date: 12/05/2018
ms.keywords: CLUSTER_RESOURCE_EMBEDDED_FAILURE_ACTION, CLUSTER_RESOURCE_EMBEDDED_FAILURE_ACTION enumeration [Failover Cluster], ClusterResourceEmbeddedFailureActionLogOnly, ClusterResourceEmbeddedFailureActionNone, ClusterResourceEmbeddedFailureActionRecover, clusapi/CLUSTER_RESOURCE_EMBEDDED_FAILURE_ACTION, clusapi/ClusterResourceEmbeddedFailureActionLogOnly, clusapi/ClusterResourceEmbeddedFailureActionNone, clusapi/ClusterResourceEmbeddedFailureActionRecover, msclus/CLUSTER_RESOURCE_EMBEDDED_FAILURE_ACTION, msclus/ClusterResourceEmbeddedFailureActionLogOnly, msclus/ClusterResourceEmbeddedFailureActionNone, msclus/ClusterResourceEmbeddedFailureActionRecover, mscs.cluster_resource_embedded_failure_action
req.header: msclus.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
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
req.typenames: CLUSTER_RESOURCE_EMBEDDED_FAILURE_ACTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_RESOURCE_EMBEDDED_FAILURE_ACTION
 - msclus/CLUSTER_RESOURCE_EMBEDDED_FAILURE_ACTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
 - MSClus.h
api_name:
 - CLUSTER_RESOURCE_EMBEDDED_FAILURE_ACTION
---

# CLUSTER_RESOURCE_EMBEDDED_FAILURE_ACTION enumeration


## -description

Specifies the various actions that can be performed when a resource has an embedded failure.

## -enum-fields

### -field ClusterResourceEmbeddedFailureActionNone:0

Indicates that no action is to be taken.

### -field ClusterResourceEmbeddedFailureActionLogOnly:1

Indicates that the failure is to be logged.

### -field ClusterResourceEmbeddedFailureActionRecover

Indicates that the resource is to be recovered.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>
