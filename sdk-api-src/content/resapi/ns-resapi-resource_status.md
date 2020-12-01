---
UID: NS:resapi.RESOURCE_STATUS
title: RESOURCE_STATUS (resapi.h)
description: Contains information about a resource that is being brought online or taken offline. This structure is used as a parameter to the callback function SetResourceStatus.
helpviewer_keywords: ["*PRESOURCE_STATUS","ClusterResourceFailed","ClusterResourceOffline","ClusterResourceOfflinePending","ClusterResourceOnline","ClusterResourceOnlinePending","ClusterResourceStateUnknown","PRESOURCE_STATUS","PRESOURCE_STATUS structure pointer [Failover Cluster]","RESOURCE_STATUS","RESOURCE_STATUS structure [Failover Cluster]","_wolf_resource_status","mscs.resource_status","resapi/PRESOURCE_STATUS","resapi/RESOURCE_STATUS"]
old-location: mscs\resource_status.htm
tech.root: MsCS
ms.assetid: a5acd51f-714f-481b-85e2-ac82b76d21bb
ms.date: 12/05/2018
ms.keywords: '*PRESOURCE_STATUS, ClusterResourceFailed, ClusterResourceOffline, ClusterResourceOfflinePending, ClusterResourceOnline, ClusterResourceOnlinePending, ClusterResourceStateUnknown, PRESOURCE_STATUS, PRESOURCE_STATUS structure pointer [Failover Cluster], RESOURCE_STATUS, RESOURCE_STATUS structure [Failover Cluster], _wolf_resource_status, mscs.resource_status, resapi/PRESOURCE_STATUS, resapi/RESOURCE_STATUS'
req.header: resapi.h
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
req.typenames: RESOURCE_STATUS, *PRESOURCE_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RESOURCE_STATUS
 - resapi/RESOURCE_STATUS
 - PRESOURCE_STATUS
 - resapi/PRESOURCE_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ResApi.h
api_name:
 - RESOURCE_STATUS
---

# RESOURCE_STATUS structure


## -description

Contains information 
    about a <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> that is being brought online or taken offline. 
    This structure is used as a parameter to the callback function 
    <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pset_resource_status_routine">SetResourceStatus</a>.

## -struct-fields

### -field ResourceState

A value describing the state of a resource enumerated by the 
       <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_state">CLUSTER_RESOURCE_STATE</a> enumeration.  The possible values for this member are as follows:



#### ClusterResourceStateUnknown (-1)

An error occurred while trying to retrieve the state, typically because the server is no longer available. 
         For more information, the caller should call the function 
         <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.



#### ClusterResourceOnline (2)

The resource is online and available.



#### ClusterResourceOffline (3)

The resource is offline and unavailable.



#### ClusterResourceFailed (4)

The resource has failed.



#### ClusterResourceOnlinePending (129)

The resource is in the process of being placed online. The <b>CheckPoint</b> member 
         should be greater than the previous value of this member.



#### ClusterResourceOfflinePending (130)

The resource is in the process of being taken offline.

### -field CheckPoint

A value set by the <a href="/previous-versions/windows/desktop/mscs/resource-dlls">resource DLL</a> to flag a status 
      report as new.

### -field WaitHint

This member is not being used at this time.

### -field EventHandle

Handle to an event that indicates when the resource has failed.

## -remarks

Resource DLLs typically set the <b>ResourceState</b> member to 
     <b>ClusterResourceOnline</b> or <b>ClusterResourceOffline</b>. However, 
     if <b>ResourceState</b> is set to <b>ClusterResourceOnlinePending</b> or 
     <b>ClusterResourceOfflinePending</b>, the <b>CheckPoint</b> member 
     should be greater than the previous value reported for <b>CheckPoint</b>.

Resource DLLs initially set <b>CheckPoint</b> to zero, then increment it by 1 for each call 
     to <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pset_resource_status_routine">SetResourceStatus</a>. 
     <a href="/previous-versions/windows/desktop/mscs/resource-monitor">Resource Monitors</a> detect new status reports by comparing 
     the current value of <b>CheckPoint</b> to the previous value. If the value has changed, the 
     Resource Monitor reads the new status information.

Before returning the <b>ClusterResourceUnknown</b> state in the 
     <b>ResourceState</b> member, a resource DLL should call the function 
     <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a>.

Resource DLLs set the <b>EventHandle</b> member to a handle that is signaled when a 
     resource fails.

For more information, see 
     <a href="/previous-versions/windows/desktop/mscs/implementing-resource-dlls">Implementing Resource DLLs</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_state">CLUSTER_RESOURCE_STATE</a>



<a href="/previous-versions/windows/desktop/mscs/resource-dll-structures">Resource DLL Structures</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pset_resource_status_routine">SetResourceStatus</a>