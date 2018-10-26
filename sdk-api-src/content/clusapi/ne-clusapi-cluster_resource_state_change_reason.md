---
UID: NE:clusapi.CLUSTER_RESOURCE_STATE_CHANGE_REASON
title: CLUSTER_RESOURCE_STATE_CHANGE_REASON
author: windows-sdk-content
description: Used by the CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT and CLUSCTL_RESOURCE_STATE_CHANGE_REASON control codes to describe the reason for a resource state change.
old-location: mscs\cluster_resource_state_change_reason.htm
tech.root: mscs
ms.assetid: f9071688-24c2-4b00-ac66-6cf0363bccf2
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: CLUSTER_RESOURCE_STATE_CHANGE_REASON, CLUSTER_RESOURCE_STATE_CHANGE_REASON enumeration [Failover Cluster], _CLUSTER_RESOURCE_STATE_CHANGE_REASON, _CLUSTER_RESOURCE_STATE_CHANGE_REASON enumeration [Failover Cluster], clusapi/CLUSTER_RESOURCE_STATE_CHANGE_REASON, clusapi/_CLUSTER_RESOURCE_STATE_CHANGE_REASON, clusapi/eResourceStateChangeReasonFailedMove, clusapi/eResourceStateChangeReasonFailover, clusapi/eResourceStateChangeReasonMove, clusapi/eResourceStateChangeReasonRundown, clusapi/eResourceStateChangeReasonShutdown, clusapi/eResourceStateChangeReasonUnknown, eResourceStateChangeReasonFailedMove, eResourceStateChangeReasonFailover, eResourceStateChangeReasonMove, eResourceStateChangeReasonRundown, eResourceStateChangeReasonShutdown, eResourceStateChangeReasonUnknown, msclus/CLUSTER_RESOURCE_STATE_CHANGE_REASON, msclus/_CLUSTER_RESOURCE_STATE_CHANGE_REASON, msclus/eResourceStateChangeReasonFailedMove, msclus/eResourceStateChangeReasonFailover, msclus/eResourceStateChangeReasonMove, msclus/eResourceStateChangeReasonRundown, msclus/eResourceStateChangeReasonShutdown, msclus/eResourceStateChangeReasonUnknown, mscs.cluster_resource_state_change_reason
ms.prod: windows
ms.technology: windows-sdk
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
    <a href="https://msdn.microsoft.com/en-us/library/Aa367493(v=VS.85).aspx">CLUSCTL_RESOURCE_STATE_CHANGE_REASON</a> 
    control codes to describe the reason for a resource state change.


## -enum-fields




### -field eResourceStateChangeReasonUnknown

This reason code is never sent by the cluster. 
       <a href="https://msdn.microsoft.com/en-us/library/Aa372239(v=VS.85).aspx">Resource DLLs</a> should use this value to initialize a local 
       <a href="https://msdn.microsoft.com/en-us/library/Aa367494(v=VS.85).aspx">CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT</a> structure and to reset the 
       <b>eReason</b> member of the 
       <b>CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT</b> 
       structure before returning from the <a href="https://msdn.microsoft.com/en-us/library/Aa371767(v=VS.85).aspx">Offline</a> and 
       <a href="https://msdn.microsoft.com/en-us/library/Aa372939(v=VS.85).aspx">Terminate</a> entry point functions. For more information, 
       see 
       <a href="https://msdn.microsoft.com/en-us/library/Aa367493(v=VS.85).aspx">CLUSCTL_RESOURCE_STATE_CHANGE_REASON</a>.


### -field eResourceStateChangeReasonMove


<a href="https://msdn.microsoft.com/en-us/library/Aa371767(v=VS.85).aspx">Offline</a> is about to be called because the 
       <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource's</a> <a href="https://msdn.microsoft.com/en-us/library/Aa369645(v=VS.85).aspx">group</a> is being moved.


### -field eResourceStateChangeReasonFailover


<a href="https://msdn.microsoft.com/en-us/library/Aa372939(v=VS.85).aspx">Terminate</a> is about to be called because the resource's 
       group is being <a href="https://msdn.microsoft.com/en-us/library/Aa369573(v=VS.85).aspx">failed over</a>.


### -field eResourceStateChangeReasonFailedMove


<a href="https://msdn.microsoft.com/en-us/library/Aa371767(v=VS.85).aspx">Online</a> is about to be called because the resource's 
       group did not successfully complete a move operation.


### -field eResourceStateChangeReasonShutdown


<a href="https://msdn.microsoft.com/en-us/library/Aa371767(v=VS.85).aspx">Offline</a> is about to be called because the 
       <a href="https://msdn.microsoft.com/en-us/library/Aa369163(v=VS.85).aspx">Cluster service</a> is being shut down.


### -field eResourceStateChangeReasonRundown


<a href="https://msdn.microsoft.com/en-us/library/Aa372939(v=VS.85).aspx">Terminate</a> is about to be called because the Cluster 
       service has stopped unexpectedly.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb309147(v=VS.85).aspx">Failover Cluster Enumerations</a>
 

 

