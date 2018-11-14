---
UID: NF:clusapi.GetClusterGroupState
title: GetClusterGroupState function
author: windows-sdk-content
description: Returns the current state of a group.
old-location: mscs\getclustergroupstate.htm
tech.root: mscs
ms.assetid: 5f794dee-aeee-4906-ba63-c154bfda4d17
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: GetClusterGroupState, GetClusterGroupState function [Failover Cluster], PCLUSAPI_GET_CLUSTER_GROUP_STATE, PCLUSAPI_GET_CLUSTER_GROUP_STATE function [Failover Cluster], _wolf_getclustergroupstate, clusapi/GetClusterGroupState, clusapi/PCLUSAPI_GET_CLUSTER_GROUP_STATE, mscs.getclustergroupstate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - GetClusterGroupState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetClusterGroupState
: 
---

# GetClusterGroupState function


## -description


Returns the 
    current state of a <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">group</a>. The <b>PCLUSAPI_GET_CLUSTER_GROUP_STATE</b> type defines a pointer to this function.


## -parameters




### -param hGroup [in]

Handle to the group for which state information should be returned.


### -param lpszNodeName [out, optional]

Pointer to a null-terminated Unicode string containing the name of the node that currently owns the group.


### -param lpcchNodeName [in, out, optional]

Pointer to the size of the <i>lpszNodeName</i> buffer as a count of characters. On input, 
       specify the maximum number of characters the buffer can hold, including the terminating 
       <b>NULL</b>. On output, specifies the number of characters in the resulting name, excluding 
       the terminating <b>NULL</b>.


## -returns



<b>GetClusterGroupState</b> returns the current 
       state of the group, which is represented by one of the following values.




## -remarks



Note that <i>lpcchName</i> refers to a count of characters and not a count of bytes, and 
     that the returned size does not include the terminating <b>NULL</b> in the count. For more 
     information on sizing buffers, see 
     <a href="https://msdn.microsoft.com/283dc560-d547-4b42-b45c-435045080639">Data Size Conventions</a>.

Do not call <b>GetClusterGroupState</b> from any 
     resource DLL entry point function. 
     <b>GetClusterGroupState</b> can safely be called from a 
     worker thread. For more information, see 
     <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/1dbc5494-a830-4ee7-b982-48792ad87c51">CLUSTER_GROUP_STATE</a>



<a href="https://msdn.microsoft.com/bd5dee18-a06f-4e46-a27e-c907b1c25a68">CLUSTER_RESOURCE_STATE</a>



<a href="https://msdn.microsoft.com/a2336594-ac24-476e-94e8-460a31c1f643">Group Management Functions</a>



<a href="https://msdn.microsoft.com/0c7ef9d9-d32b-448e-9e07-6befb9b3e338">OpenClusterGroup</a>
 

 

