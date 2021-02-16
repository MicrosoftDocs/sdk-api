---
UID: NS:clusapi._CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT
title: CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT (clusapi.h)
description: Sent with the CLUSCTL_RESOURCE_STATE_CHANGE_REASON control code to provide the reason for a resource state change.
helpviewer_keywords: ["*PCLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT","CLUSCTL_RESOURCE_STATE_CHANGE_REASON","CLUSCTL_RESOURCE_STATE_CHANGE_REASON structure [Failover Cluster]","CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT","CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT structure [Failover Cluster]","PCLUSCTL_RESOURCE_STATE_CHANGE_REASON","PCLUSCTL_RESOURCE_STATE_CHANGE_REASON structure pointer [Failover Cluster]","_wolf_clusctl_resource_state_change_reason_struct","clusapi/CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT","clusapi/PCLUSCTL_RESOURCE_STATE_CHANGE_REASON","eResourceStateChangeReasonFailedMove","eResourceStateChangeReasonFailover","eResourceStateChangeReasonMove","eResourceStateChangeReasonRundown","eResourceStateChangeReasonShutdown","eResourceStateChangeReasonUnknown","mscs.clusctl_resource_state_change_reason_struct"]
old-location: mscs\clusctl_resource_state_change_reason_struct.htm
tech.root: MsCS
ms.assetid: 5effbb81-eec4-4e5a-b079-b404df8fd801
ms.date: 12/05/2018
ms.keywords: '*PCLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT, CLUSCTL_RESOURCE_STATE_CHANGE_REASON, CLUSCTL_RESOURCE_STATE_CHANGE_REASON structure [Failover Cluster], CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT, CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT structure [Failover Cluster], PCLUSCTL_RESOURCE_STATE_CHANGE_REASON, PCLUSCTL_RESOURCE_STATE_CHANGE_REASON structure pointer [Failover Cluster], _wolf_clusctl_resource_state_change_reason_struct, clusapi/CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT, clusapi/PCLUSCTL_RESOURCE_STATE_CHANGE_REASON, eResourceStateChangeReasonFailedMove, eResourceStateChangeReasonFailover, eResourceStateChangeReasonMove, eResourceStateChangeReasonRundown, eResourceStateChangeReasonShutdown, eResourceStateChangeReasonUnknown, mscs.clusctl_resource_state_change_reason_struct'
req.header: clusapi.h
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
req.typenames: CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT, *PCLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT
 - clusapi/_CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT
 - PCLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT
 - clusapi/PCLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT
 - CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT
 - clusapi/CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSCTL_RESOURCE_STATE_CHANGE_REASON
---

# CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT structure


## -description

Sent with the 
    <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-state-change-reason">CLUSCTL_RESOURCE_STATE_CHANGE_REASON</a> 
    control code to provide the reason for a <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> state 
    change.

## -struct-fields

### -field dwSize

The size of the structure in bytes.

### -field dwVersion

The version of the structure. Set to 
       <b>CLUSCTL_RESOURCE_STATE_CHANGE_REASON_VERSION_1</b> (1).

### -field eReason

A value of the 
      <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_state_change_reason">CLUSTER_RESOURCE_STATE_CHANGE_REASON</a> 
      enumeration that describes the reason for the state change. The following list lists the possible values.



#### eResourceStateChangeReasonUnknown (0)

This reason code is never sent by the cluster. 
         <a href="/previous-versions/windows/desktop/mscs/resource-dlls">Resource DLLs</a> should use this value to initialize a 
         local 
         <b>CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT</b> 
         structure and to reset the <b>eReason</b> member of this structure before returning from 
         the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a> 
         and <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pterminate_routine">Terminate</a> entry point functions. For more 
         information, see 
         <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-state-change-reason">CLUSCTL_RESOURCE_STATE_CHANGE_REASON</a>.



#### eResourceStateChangeReasonMove (1)


<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a> is about to be called because the 
         <a href="/previous-versions/windows/desktop/mscs/resources">resource's</a> <a href="/previous-versions/windows/desktop/mscs/groups">group</a> is being moved.



#### eResourceStateChangeReasonFailover (2)


<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pterminate_routine">Terminate</a> is about to be called because the 
         resource's group is being <a href="/previous-versions/windows/desktop/mscs/failover">failed over</a>.



#### eResourceStateChangeReasonFailedMove (3)


<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Online</a> is about to be called because the resource's 
         group did not successfully complete a move operation.



#### eResourceStateChangeReasonShutdown (4)


<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a> is about to be called because the 
         <a href="/previous-versions/windows/desktop/mscs/cluster-service">Cluster service</a> is being shut down.



#### eResourceStateChangeReasonRundown (5)


<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pterminate_routine">Terminate</a> is about to be called because the Cluster 
         service has stopped unexpectedly.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_state_change_reason">CLUSTER_RESOURCE_STATE_CHANGE_REASON</a>



<a href="/previous-versions/windows/desktop/mscs/utility-structures">Utility Structures</a>