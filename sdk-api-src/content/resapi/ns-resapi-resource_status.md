---
UID: NS:resapi.RESOURCE_STATUS
title: RESOURCE_STATUS
author: windows-driver-content
description: Contains information about a resource that is being brought online or taken offline. This structure is used as a parameter to the callback function SetResourceStatus.
old-location: mscs\resource_status.htm
old-project: MsCS
ms.assetid: a5acd51f-714f-481b-85e2-ac82b76d21bb
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: "*PRESOURCE_STATUS, ClusterResourceFailed, ClusterResourceOffline, ClusterResourceOfflinePending, ClusterResourceOnline, ClusterResourceOnlinePending, ClusterResourceStateUnknown, PRESOURCE_STATUS, PRESOURCE_STATUS structure pointer [Failover Cluster], RESOURCE_STATUS, RESOURCE_STATUS structure [Failover Cluster], _wolf_resource_status, mscs.resource_status, resapi/PRESOURCE_STATUS, resapi/RESOURCE_STATUS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: RESOURCE_STATUS, *PRESOURCE_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ResApi.h
api_name:
-	RESOURCE_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RESOURCE_STATUS structure


## -description


Contains information 
    about a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> that is being brought online or taken offline. 
    This structure is used as a parameter to the callback function 
    <a href="https://msdn.microsoft.com/8ddb4578-f8c4-462e-af04-8c537d585e8b">SetResourceStatus</a>.


## -struct-fields




### -field ResourceState

A value describing the state of a resource enumerated by the 
       <a href="https://msdn.microsoft.com/bd5dee18-a06f-4e46-a27e-c907b1c25a68">CLUSTER_RESOURCE_STATE</a> enumeration.  The possible values for this member are as follows:



#### ClusterResourceStateUnknown (-1)

An error occurred while trying to retrieve the state, typically because the server is no longer available. 
         For more information, the caller should call the function 
         <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



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

A value set by the <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">resource DLL</a> to flag a status 
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
     to <a href="https://msdn.microsoft.com/8ddb4578-f8c4-462e-af04-8c537d585e8b">SetResourceStatus</a>. 
     <a href="https://msdn.microsoft.com/caebb47f-c2c5-463e-a957-d9eefc7fc33d">Resource Monitors</a> detect new status reports by comparing 
     the current value of <b>CheckPoint</b> to the previous value. If the value has changed, the 
     Resource Monitor reads the new status information.

Before returning the <b>ClusterResourceUnknown</b> state in the 
     <b>ResourceState</b> member, a resource DLL should call the function 
     <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a>.

Resource DLLs set the <b>EventHandle</b> member to a handle that is signaled when a 
     resource fails.

For more information, see 
     <a href="https://msdn.microsoft.com/400862c3-73c4-443d-bc60-1c1b6b34534f">Implementing Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/bd5dee18-a06f-4e46-a27e-c907b1c25a68">CLUSTER_RESOURCE_STATE</a>



<a href="https://msdn.microsoft.com/9ab4b974-28b5-4f33-a7c4-b9b2472059aa">Resource DLL Structures</a>



<a href="https://msdn.microsoft.com/8ddb4578-f8c4-462e-af04-8c537d585e8b">SetResourceStatus</a>
 

 

