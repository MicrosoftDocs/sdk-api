---
UID: NS:clusapi._CLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT
title: "_CLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT"
author: windows-sdk-content
description: Specifies information about the last time a group was moved to another node.
old-location: mscs\clusctl_group_get_last_move_time_output.htm
tech.root: mscs
ms.assetid: C8292546-4220-4A5D-91C6-03687DD06A9B
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PCLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT, CLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT, CLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT structure [Failover Cluster], PCLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT, PCLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT structure pointer [Failover Cluster], _CLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT, clusapi/CLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT, clusapi/PCLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT, mscs.clusctl_group_get_last_move_time_output"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
 - CLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT
product: Windows
targetos: Windows
req.typenames: CLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT, *PCLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT
req.redist: 
---

# _CLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT structure


## -description


Specifies information about the last time a group was moved to another node.


## -struct-fields




### -field GetTickCount64

The number of milliseconds that have elapsed in the owning node, when the group was moved.


### -field GetSystemTime

The system date and time in the owning node, when the group was moved.


### -field NodeId

The unique ID of the node that owns the group.


## -see-also




<a href="https://msdn.microsoft.com/9ed8386b-f035-446f-b0f8-12e0d3f23aac">GetSystemTime</a>



<a href="https://msdn.microsoft.com/3ebf05b9-cc53-43ae-bbcb-7841793a9d84">GetTickCount64</a>



<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa373109(v=VS.85).aspx">Utility Structures</a>
 

 

