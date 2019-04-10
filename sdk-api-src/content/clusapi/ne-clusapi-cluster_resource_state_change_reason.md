---
UID: NE:clusapi.CLUSTER_RESOURCE_STATE_CHANGE_REASON
title: CLUSTER_RESOURCE_STATE_CHANGE_REASON (clusapi.h)
author: windows-sdk-content
description: Used by the CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT and CLUSCTL_RESOURCE_STATE_CHANGE_REASON control codes to describe the reason for a resource state change.
old-location: mscs\cluster_resource_state_change_reason.htm
tech.root: MsCS
ms.assetid: f9071688-24c2-4b00-ac66-6cf0363bccf2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CLUSTER_RESOURCE_STATE_CHANGE_REASON, CLUSTER_RESOURCE_STATE_CHANGE_REASON enumeration [Failover Cluster], _CLUSTER_RESOURCE_STATE_CHANGE_REASON, _CLUSTER_RESOURCE_STATE_CHANGE_REASON enumeration [Failover Cluster], clusapi/CLUSTER_RESOURCE_STATE_CHANGE_REASON, clusapi/_CLUSTER_RESOURCE_STATE_CHANGE_REASON, clusapi/eResourceStateChangeReasonFailedMove, clusapi/eResourceStateChangeReasonFailover, clusapi/eResourceStateChangeReasonMove, clusapi/eResourceStateChangeReasonRundown, clusapi/eResourceStateChangeReasonShutdown, clusapi/eResourceStateChangeReasonUnknown, eResourceStateChangeReasonFailedMove, eResourceStateChangeReasonFailover, eResourceStateChangeReasonMove, eResourceStateChangeReasonRundown, eResourceStateChangeReasonShutdown, eResourceStateChangeReasonUnknown, msclus/CLUSTER_RESOURCE_STATE_CHANGE_REASON, msclus/_CLUSTER_RESOURCE_STATE_CHANGE_REASON, msclus/eResourceStateChangeReasonFailedMove, msclus/eResourceStateChangeReasonFailover, msclus/eResourceStateChangeReasonMove, msclus/eResourceStateChangeReasonRundown, msclus/eResourceStateChangeReasonShutdown, msclus/eResourceStateChangeReasonUnknown, mscs.cluster_resource_state_change_reason
ms.topic: enum
req.header: clusapi.h
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
product: Windows
targetos: Windows
req.typenames: CLUSTER_RESOURCE_STATE_CHANGE_REASON
req.redist: 
---

# CLUSTER_RESOURCE_STATE_CHANGE_REASON enumeration


## -description


Used by the 
    <a href="https://msdn.microsoft.com/en-us/library/Aa367494(v=VS.85).aspx">CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT</a> 
    and  
    <a href="https://msdn.microsoft.com/3261c8eb-b88b-428a-8a2b-684e0967f9de">CLUSCTL_RESOURCE_STATE_CHANGE_REASON</a> 
    control codes to describe the reason for a resource state change.


## -enum-fields




### -field eResourceStateChangeReasonUnknown

This reason code is never sent by the cluster. 
       <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">Resource DLLs</a> should use this value to initialize a local 
       <a href="https://msdn.microsoft.com/en-us/library/Aa367494(v=VS.85).aspx">CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT</a> structure and to reset the 
       <b>eReason</b> member of the 
       <b>CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT</b> 
       structure before returning from the <a href="https://msdn.microsoft.com/1d67a4f5-66f8-4818-8b63-d0f50452f889">Offline</a> and 
       <a href="https://msdn.microsoft.com/b53ab7db-ed17-4386-8a5f-5d0b0d1cb1b3">Terminate</a> entry point functions. For more information, 
       see 
       <a href="https://msdn.microsoft.com/3261c8eb-b88b-428a-8a2b-684e0967f9de">CLUSCTL_RESOURCE_STATE_CHANGE_REASON</a>.


### -field eResourceStateChangeReasonMove


<a href="https://msdn.microsoft.com/1d67a4f5-66f8-4818-8b63-d0f50452f889">Offline</a> is about to be called because the 
       <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource's</a> <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">group</a> is being moved.


### -field eResourceStateChangeReasonFailover


<a href="https://msdn.microsoft.com/b53ab7db-ed17-4386-8a5f-5d0b0d1cb1b3">Terminate</a> is about to be called because the resource's 
       group is being <a href="https://msdn.microsoft.com/6722d075-02e0-4817-abc3-dce8951c17da">failed over</a>.


### -field eResourceStateChangeReasonFailedMove


<a href="https://msdn.microsoft.com/1d67a4f5-66f8-4818-8b63-d0f50452f889">Online</a> is about to be called because the resource's 
       group did not successfully complete a move operation.


### -field eResourceStateChangeReasonShutdown


<a href="https://msdn.microsoft.com/1d67a4f5-66f8-4818-8b63-d0f50452f889">Offline</a> is about to be called because the 
       <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a> is being shut down.


### -field eResourceStateChangeReasonRundown


<a href="https://msdn.microsoft.com/b53ab7db-ed17-4386-8a5f-5d0b0d1cb1b3">Terminate</a> is about to be called because the Cluster 
       service has stopped unexpectedly.


## -see-also




<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

