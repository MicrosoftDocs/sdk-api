---
UID: NE:msclus.CLUSTER_RESOURCE_STATE_CHANGE_REASON
title: CLUSTER_RESOURCE_STATE_CHANGE_REASON (msclus.h)
description: Used by the CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT and CLUSCTL_RESOURCE_STATE_CHANGE_REASON control codes to describe the reason for a resource state change.
helpviewer_keywords: ["CLUSTER_RESOURCE_STATE_CHANGE_REASON","CLUSTER_RESOURCE_STATE_CHANGE_REASON enumeration [Failover Cluster]","_CLUSTER_RESOURCE_STATE_CHANGE_REASON","_CLUSTER_RESOURCE_STATE_CHANGE_REASON enumeration [Failover Cluster]","clusapi/CLUSTER_RESOURCE_STATE_CHANGE_REASON","clusapi/_CLUSTER_RESOURCE_STATE_CHANGE_REASON","clusapi/eResourceStateChangeReasonFailedMove","clusapi/eResourceStateChangeReasonFailover","clusapi/eResourceStateChangeReasonMove","clusapi/eResourceStateChangeReasonRundown","clusapi/eResourceStateChangeReasonShutdown","clusapi/eResourceStateChangeReasonUnknown","eResourceStateChangeReasonFailedMove","eResourceStateChangeReasonFailover","eResourceStateChangeReasonMove","eResourceStateChangeReasonRundown","eResourceStateChangeReasonShutdown","eResourceStateChangeReasonUnknown","msclus/CLUSTER_RESOURCE_STATE_CHANGE_REASON","msclus/_CLUSTER_RESOURCE_STATE_CHANGE_REASON","msclus/eResourceStateChangeReasonFailedMove","msclus/eResourceStateChangeReasonFailover","msclus/eResourceStateChangeReasonMove","msclus/eResourceStateChangeReasonRundown","msclus/eResourceStateChangeReasonShutdown","msclus/eResourceStateChangeReasonUnknown","mscs.cluster_resource_state_change_reason"]
old-location: mscs\cluster_resource_state_change_reason.htm
tech.root: MsCS
ms.assetid: f9071688-24c2-4b00-ac66-6cf0363bccf2
ms.date: 12/05/2018
ms.keywords: CLUSTER_RESOURCE_STATE_CHANGE_REASON, CLUSTER_RESOURCE_STATE_CHANGE_REASON enumeration [Failover Cluster], _CLUSTER_RESOURCE_STATE_CHANGE_REASON, _CLUSTER_RESOURCE_STATE_CHANGE_REASON enumeration [Failover Cluster], clusapi/CLUSTER_RESOURCE_STATE_CHANGE_REASON, clusapi/_CLUSTER_RESOURCE_STATE_CHANGE_REASON, clusapi/eResourceStateChangeReasonFailedMove, clusapi/eResourceStateChangeReasonFailover, clusapi/eResourceStateChangeReasonMove, clusapi/eResourceStateChangeReasonRundown, clusapi/eResourceStateChangeReasonShutdown, clusapi/eResourceStateChangeReasonUnknown, eResourceStateChangeReasonFailedMove, eResourceStateChangeReasonFailover, eResourceStateChangeReasonMove, eResourceStateChangeReasonRundown, eResourceStateChangeReasonShutdown, eResourceStateChangeReasonUnknown, msclus/CLUSTER_RESOURCE_STATE_CHANGE_REASON, msclus/_CLUSTER_RESOURCE_STATE_CHANGE_REASON, msclus/eResourceStateChangeReasonFailedMove, msclus/eResourceStateChangeReasonFailover, msclus/eResourceStateChangeReasonMove, msclus/eResourceStateChangeReasonRundown, msclus/eResourceStateChangeReasonShutdown, msclus/eResourceStateChangeReasonUnknown, mscs.cluster_resource_state_change_reason
req.header: msclus.h
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
req.typenames: CLUSTER_RESOURCE_STATE_CHANGE_REASON
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_RESOURCE_STATE_CHANGE_REASON
 - msclus/CLUSTER_RESOURCE_STATE_CHANGE_REASON
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
 - CLUSTER_RESOURCE_STATE_CHANGE_REASON
---

# CLUSTER_RESOURCE_STATE_CHANGE_REASON enumeration


## -description

Used by the 
    <a href="/windows/win32/api/clusapi/ns-clusapi-clusctl_resource_state_change_reason_struct">CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT</a> 
    and  
    <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-state-change-reason">CLUSCTL_RESOURCE_STATE_CHANGE_REASON</a> 
    control codes to describe the reason for a resource state change.

## -enum-fields

### -field eResourceStateChangeReasonUnknown:0

This reason code is never sent by the cluster. 
       <a href="/previous-versions/windows/desktop/mscs/resource-dlls">Resource DLLs</a> should use this value to initialize a local 
       <a href="/windows/win32/api/clusapi/ns-clusapi-clusctl_resource_state_change_reason_struct">CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT</a> structure and to reset the 
       <b>eReason</b> member of the 
       <b>CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT</b> 
       structure before returning from the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a> and 
       <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pterminate_routine">Terminate</a> entry point functions. For more information, 
       see 
       <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-state-change-reason">CLUSCTL_RESOURCE_STATE_CHANGE_REASON</a>.

### -field eResourceStateChangeReasonMove

<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a> is about to be called because the 
       <a href="/previous-versions/windows/desktop/mscs/resources">resource's</a> <a href="/previous-versions/windows/desktop/mscs/groups">group</a> is being moved.

### -field eResourceStateChangeReasonFailover

<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pterminate_routine">Terminate</a> is about to be called because the resource's 
       group is being <a href="/previous-versions/windows/desktop/mscs/failover">failed over</a>.

### -field eResourceStateChangeReasonFailedMove

<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Online</a> is about to be called because the resource's 
       group did not successfully complete a move operation.

### -field eResourceStateChangeReasonShutdown

<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a> is about to be called because the 
       <a href="/previous-versions/windows/desktop/mscs/cluster-service">Cluster service</a> is being shut down.

### -field eResourceStateChangeReasonRundown

<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pterminate_routine">Terminate</a> is about to be called because the Cluster 
       service has stopped unexpectedly.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>
