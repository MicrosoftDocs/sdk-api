---
UID: NF:clusapi.GetClusterGroupState
title: GetClusterGroupState function (clusapi.h)
author: windows-sdk-content
description: Returns the current state of a group.
old-location: mscs\getclustergroupstate.htm
tech.root: MsCS
ms.assetid: 5f794dee-aeee-4906-ba63-c154bfda4d17
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetClusterGroupState, GetClusterGroupState function [Failover Cluster], PCLUSAPI_GET_CLUSTER_GROUP_STATE, PCLUSAPI_GET_CLUSTER_GROUP_STATE function [Failover Cluster], _wolf_getclustergroupstate, clusapi/GetClusterGroupState, clusapi/PCLUSAPI_GET_CLUSTER_GROUP_STATE, mscs.getclustergroupstate
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

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterGroupStateUnknown</b></dt>
<dt>-1</dt>
</dl>
</td>
<td width="60%">
The operation was not successful. For more information about the error, call the function 
         <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterGroupOnline</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
All of the resources in the group are <a href="https://msdn.microsoft.com/en-us/library/Aa371781(v=VS.85).aspx">online</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterGroupOffline</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
All of the resources in the group are <a href="https://msdn.microsoft.com/en-us/library/Aa371781(v=VS.85).aspx">offline</a> or 
         there are no resources in the group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterGroupFailed</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
At least one <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> in the group has failed (set a state 
         of <b>ClusterResourceFailed</b> from the <a href="https://msdn.microsoft.com/bd5dee18-a06f-4e46-a27e-c907b1c25a68">CLUSTER_RESOURCE_STATE</a> enumeration).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterGroupPartialOnline</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
At least one resource in the group is online. No resources are 
         <a href="https://msdn.microsoft.com/en-us/library/Aa371816(v=VS.85).aspx">pending</a> or 
         <a href="https://msdn.microsoft.com/en-us/library/Aa369590(v=VS.85).aspx">failed</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterGroupPending</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
At least one resource in the group is in a pending state. There are no failed resources.

</td>
</tr>
</table>
 




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
 

 

