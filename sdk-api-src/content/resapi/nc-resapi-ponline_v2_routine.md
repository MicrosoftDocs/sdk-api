---
UID: NC:resapi.PONLINE_V2_ROUTINE
title: PONLINE_V2_ROUTINE
author: windows-driver-content
description: Marks a resource as available for use.
old-location: mscs\onlinev2.htm
old-project: MsCS
ms.assetid: 0462CDFD-6499-4FF8-8B5C-4DC15AC30169
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: CLUS_RESDLL_ONLINE_IGNORE_NETWORK_CONNECTIVITY, CLUS_RESDLL_ONLINE_IGNORE_RESOURCE_STATUS, CLUS_RESDLL_ONLINE_RECOVER_MONITOR_STATE, CLUS_RESDLL_ONLINE_RESTORE_ONLINE_STATE, CLUS_RESDLL_ONLINE_RETURN_TO_SOURCE_NODE_ON_ERROR, OnlineV2, OnlineV2 callback function [Failover Cluster], PONLINE_V2_ROUTINE, PONLINE_V2_ROUTINE callback function [Failover Cluster], mscs.onlinev2, resapi/OnlineV2, resapi/PONLINE_V2_ROUTINE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ResApi.h
api_name:
-	OnlineV2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PONLINE_V2_ROUTINE callback


## -description


Marks a 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> as available for use. The 
    <b>PONLINE_V2_ROUTINE</b> type defines a pointer to this function.


## -parameters




### -param Resource [in]

A resource identifier for the resource to be made available.


### -param EventHandle [out]

On input, <i>EventHandle</i> is <b>NULL</b>. On output, 
       <i>EventHandle</i> contains a handle to a non signaled 
       <a href="https://msdn.microsoft.com/11558ae9-1056-48bf-96f5-94a051df41c3">synchronization object</a>. The 
       <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">resource DLL</a> can signal this handle at any time to report 
       a resource failure to the <a href="https://msdn.microsoft.com/caebb47f-c2c5-463e-a957-d9eefc7fc33d">Resource Monitor</a>. 
       <i>EventHandle</i> can also be set to <b>NULL</b> on output, which indicates 
       that the resource does not support asynchronous event notifications.


### -param OnlineFlags [in]

A bitmask of flags that specify settings for this operation. This parameter can be set to one or more  of the following values:



#### CLUS_RESDLL_ONLINE_RECOVER_MONITOR_STATE (0x00000001)

Monitor the state of the  resource if the resource is recovering from an error.



#### CLUS_RESDLL_ONLINE_IGNORE_RESOURCE_STATUS (0x00000002)

Perform the operation even if the resource indicates that it should be locked.



#### CLUS_RESDLL_ONLINE_RETURN_TO_SOURCE_NODE_ON_ERROR (0x00000004)

If the resource experiences an error, return it to the source node.



#### CLUS_RESDLL_ONLINE_RESTORE_ONLINE_STATE (0x00000008)

Set the status of the resource to online.



#### CLUS_RESDLL_ONLINE_IGNORE_NETWORK_CONNECTIVITY (0x00000010)

Perform the operation even if there is network error.


### -param InBuffer [in, optional]

A pointer to a buffer that contains  data for the operation; otherwise <b>NULL</b> if the operation does not require data.


### -param InBufferSize [in]

The size of the <i>InBuffer</i> parameter, in bytes.


### -param Reserved [in]

Reserved.


## -returns



If the operation was not successful for other reasons, 
       a 
       system error code is returned.




## -see-also




<a href="https://msdn.microsoft.com/933d7b97-b5be-4c84-a983-41d1fd935c19">Resource DLL Entry-Point Functions</a>
 

 

