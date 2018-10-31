---
UID: NS:clusapi._CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT
title: "_CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT"
author: windows-sdk-content
description: Sent with the CLUSCTL_RESOURCE_STATE_CHANGE_REASON control code to provide the reason for a resource state change.
old-location: mscs\clusctl_resource_state_change_reason_struct.htm
tech.root: mscs
ms.assetid: 5effbb81-eec4-4e5a-b079-b404df8fd801
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PCLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT, CLUSCTL_RESOURCE_STATE_CHANGE_REASON, CLUSCTL_RESOURCE_STATE_CHANGE_REASON structure [Failover Cluster], CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT, CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT structure [Failover Cluster], PCLUSCTL_RESOURCE_STATE_CHANGE_REASON, PCLUSCTL_RESOURCE_STATE_CHANGE_REASON structure pointer [Failover Cluster], _CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT, _wolf_clusctl_resource_state_change_reason_struct, clusapi/CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT, clusapi/PCLUSCTL_RESOURCE_STATE_CHANGE_REASON, eResourceStateChangeReasonFailedMove, eResourceStateChangeReasonFailover, eResourceStateChangeReasonMove, eResourceStateChangeReasonRundown, eResourceStateChangeReasonShutdown, eResourceStateChangeReasonUnknown, mscs.clusctl_resource_state_change_reason_struct"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSCTL_RESOURCE_STATE_CHANGE_REASON
product: Windows
targetos: Windows
req.typenames: CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT, *PCLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT
req.redist: 
---

# _CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT structure


## -description


Sent with the 
    <a href="https://msdn.microsoft.com/en-us/library/Aa367493(v=VS.85).aspx">CLUSCTL_RESOURCE_STATE_CHANGE_REASON</a> 
    control code to provide the reason for a <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource</a> state 
    change.


## -struct-fields




### -field dwSize

The size of the structure in bytes.


### -field dwVersion

The version of the structure. Set to 
       <b>CLUSCTL_RESOURCE_STATE_CHANGE_REASON_VERSION_1</b> (1).


### -field eReason

A value of the 
      <a href="https://msdn.microsoft.com/en-us/library/Bb309169(v=VS.85).aspx">CLUSTER_RESOURCE_STATE_CHANGE_REASON</a> 
      enumeration that describes the reason for the state change. The following list lists the possible values.



#### eResourceStateChangeReasonUnknown (0)

This reason code is never sent by the cluster. 
         <a href="https://msdn.microsoft.com/en-us/library/Aa372239(v=VS.85).aspx">Resource DLLs</a> should use this value to initialize a 
         local 
         <b>CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT</b> 
         structure and to reset the <b>eReason</b> member of this structure before returning from 
         the <a href="https://msdn.microsoft.com/en-us/library/Aa371767(v=VS.85).aspx">Offline</a> 
         and <a href="https://msdn.microsoft.com/en-us/library/Aa372939(v=VS.85).aspx">Terminate</a> entry point functions. For more 
         information, see 
         <a href="https://msdn.microsoft.com/en-us/library/Aa367493(v=VS.85).aspx">CLUSCTL_RESOURCE_STATE_CHANGE_REASON</a>.



#### eResourceStateChangeReasonMove (1)


<a href="https://msdn.microsoft.com/en-us/library/Aa371767(v=VS.85).aspx">Offline</a> is about to be called because the 
         <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource's</a> <a href="https://msdn.microsoft.com/en-us/library/Aa369645(v=VS.85).aspx">group</a> is being moved.



#### eResourceStateChangeReasonFailover (2)


<a href="https://msdn.microsoft.com/en-us/library/Aa372939(v=VS.85).aspx">Terminate</a> is about to be called because the 
         resource's group is being <a href="https://msdn.microsoft.com/en-us/library/Aa369573(v=VS.85).aspx">failed over</a>.



#### eResourceStateChangeReasonFailedMove (3)


<a href="https://msdn.microsoft.com/en-us/library/Aa371767(v=VS.85).aspx">Online</a> is about to be called because the resource's 
         group did not successfully complete a move operation.



#### eResourceStateChangeReasonShutdown (4)


<a href="https://msdn.microsoft.com/en-us/library/Aa371767(v=VS.85).aspx">Offline</a> is about to be called because the 
         <a href="https://msdn.microsoft.com/en-us/library/Aa369163(v=VS.85).aspx">Cluster service</a> is being shut down.



#### eResourceStateChangeReasonRundown (5)


<a href="https://msdn.microsoft.com/en-us/library/Aa372939(v=VS.85).aspx">Terminate</a> is about to be called because the Cluster 
         service has stopped unexpectedly.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb309169(v=VS.85).aspx">CLUSTER_RESOURCE_STATE_CHANGE_REASON</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa373109(v=VS.85).aspx">Utility Structures</a>
 

 

