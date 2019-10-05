---
UID: NS:clusapi._CLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT
title: CLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT (clusapi.h)
author: windows-sdk-content
description: Specifies information about the last time a group was moved to another node.
old-location: mscs\clusctl_group_get_last_move_time_output.htm
tech.root: MsCS
ms.assetid: C8292546-4220-4A5D-91C6-03687DD06A9B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT, CLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT, CLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT structure [Failover Cluster], PCLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT, PCLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT structure pointer [Failover Cluster], clusapi/CLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT, clusapi/PCLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT, mscs.clusctl_group_get_last_move_time_output"
ms.topic: struct
f1_keywords: 
 - "clusapi/CLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: CLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT, *PCLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT
req.redist: 
ms.custom: 19H1
---

# CLUSCTL_GROUP_GET_LAST_MOVE_TIME_OUTPUT structure


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




<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtime">GetSystemTime</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-gettickcount64">GetTickCount64</a>



<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/utility-structures">Utility Structures</a>
 

 

