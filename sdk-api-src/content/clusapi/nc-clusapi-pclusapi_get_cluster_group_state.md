---
UID: NC:clusapi.PCLUSAPI_GET_CLUSTER_GROUP_STATE
title: PCLUSAPI_GET_CLUSTER_GROUP_STATE
author: windows-driver-content
description: Returns the current state of a group.
old-location: mscs\getclustergroupstate.htm
old-project: MsCS
ms.assetid: 5f794dee-aeee-4906-ba63-c154bfda4d17
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: PCLUSAPI_GET_CLUSTER_GROUP_STATE, PCLUSAPI_GET_CLUSTER_GROUP_STATE callback, PCLUSAPI_GET_CLUSTER_GROUP_STATE callback function [Failover Cluster], _wolf_getclustergroupstate, clusapi/PCLUSAPI_GET_CLUSTER_GROUP_STATE, mscs.getclustergroupstate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_GET_CLUSTER_GROUP_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_GET_CLUSTER_GROUP_STATE callback function


## -description


Returns the 
    current state of a <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a>. The <b>PCLUSAPI_GET_CLUSTER_GROUP_STATE</b> type defines a pointer to this function.


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



<i>GetClusterGroupState</i> returns the current 
       state of the group, which is represented by one of the following values.




## -remarks



Note that <i>lpcchName</i> refers to a count of characters and not a count of bytes, and 
     that the returned size does not include the terminating <b>NULL</b> in the count. For more 
     information on sizing buffers, see 
     <a href="https://msdn.microsoft.com/283dc560-d547-4b42-b45c-435045080639">Data Size Conventions</a>.

Do not call <i>GetClusterGroupState</i> from any 
     resource DLL entry point function. 
     <i>GetClusterGroupState</i> can safely be called from a 
     worker thread. For more information, see 
     <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/1dbc5494-a830-4ee7-b982-48792ad87c51">CLUSTER_GROUP_STATE</a>



<a href="https://msdn.microsoft.com/bd5dee18-a06f-4e46-a27e-c907b1c25a68">CLUSTER_RESOURCE_STATE</a>



<a href="https://msdn.microsoft.com/a2336594-ac24-476e-94e8-460a31c1f643">Group Management Functions</a>



<a href="https://msdn.microsoft.com/0c7ef9d9-d32b-448e-9e07-6befb9b3e338">OpenClusterGroup</a>
 

 

