---
UID: NF:clusapi.ClusterResourceEnum
title: ClusterResourceEnum function
author: windows-sdk-content
description: Enumerates a resource's dependent resources, nodes, or both.
old-location: mscs\clusterresourceenum.htm
tech.root: MsCS
ms.assetid: 73627594-90df-496d-8120-b24c34f13fb5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CLUSTER_RESOURCE_ENUM_DEPENDS, CLUSTER_RESOURCE_ENUM_NODES, CLUSTER_RESOURCE_ENUM_PROVIDES, ClusterResourceEnum, ClusterResourceEnum function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_ENUM, PCLUSAPI_CLUSTER_RESOURCE_ENUM function [Failover Cluster], _wolf_clusterresourceenum, clusapi/ClusterResourceEnum, clusapi/PCLUSAPI_CLUSTER_RESOURCE_ENUM, mscs.clusterresourceenum
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
 - Ext-MS-Win-Cluster-ClusAPI-L1-1-2.dll
api_name:
 - ClusterResourceEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ClusterResourceEnum
: 
---

# ClusterResourceEnum function


## -description


Enumerates a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource's</a> dependent resources, 
    <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">nodes</a>, or both. It returns the name of one 
    <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">cluster object</a> with each call. The <b>PCLUSAPI_CLUSTER_RESOURCE_ENUM</b> type defines a pointer to this function.


## -parameters




### -param hResEnum [in]

A resource enumeration handle returned from 
       the <a href="https://msdn.microsoft.com/f801401f-f49d-41de-b88b-b832330eeccf">ClusterResourceOpenEnum</a> function.


### -param dwIndex [in]

The index of the resource or node object to return. This parameter should be zero for the first call to the 
       <b>ClusterResourceEnum</b> function and then 
       incremented for subsequent calls.


### -param lpdwType [out]

The type of object returned by 
       <b>ClusterResourceEnum</b>.


The possible values are one of the following <a href="https://msdn.microsoft.com/8b59ab43-7e03-4ddf-82cc-9945e9da6462">CLUSTER_RESOURCE_ENUM</a> enumeration values:





#### CLUSTER_RESOURCE_ENUM_DEPENDS (1)

The object is a resource and  <i>hResEnum</i> is a resource that depends on this object.



#### CLUSTER_RESOURCE_ENUM_PROVIDES (2)

The object is a resource that depends on the resource identified by <i>hResEnum</i>.



#### CLUSTER_RESOURCE_ENUM_NODES (4)

The object is a node that can host the resource identified by <i>hResEnum</i>.


### -param lpszName [out]

A pointer to a null-terminated Unicode string containing the name of the returned object.


### -param lpcchName [in, out]

A pointer to the size of the <i>lpszName</i> buffer as a count of characters. On input, 
       specify the maximum number of characters the buffer can hold, including the terminating null character. On 
       output, specifies the number of characters in the resulting name, excluding the terminating null character.


## -returns



The function returns one of the following values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The operation completed successfully or the <i>lpszName</i> parameter is 
         <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
<dt>234 (0xEA)</dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by the <i>lpszName</i> parameter is not big enough to hold the 
         result. The <i>lpcchName</i> parameter returns the number of characters in the result, 
         excluding the terminating null character.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
<dt>259 (0x103)</dt>
</dl>
</td>
<td width="60%">
There are no more objects to be returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System error code</a></b></dt>
</dl>
</td>
<td width="60%">
Any other returned error code indicates that the operation failed.

</td>
</tr>
</table>
 




## -remarks



Note that <i>lpcchName</i> refers to a count of characters and not a count of bytes, and 
     that the returned size does not include the terminating null character in the count. For more information on 
     sizing buffers, see <a href="https://msdn.microsoft.com/283dc560-d547-4b42-b45c-435045080639">Data Size Conventions</a>.

Do not call <b>ClusterResourceEnum</b> from any 
     resource DLL entry point function. 
     <b>ClusterResourceEnum</b> can safely be called from a 
     worker thread. For more information, see 
     <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.


#### Examples

See <a href="https://msdn.microsoft.com/391b87d1-6765-45fd-bd27-37a1127e639a">Enumerating Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d1f7360d-f592-49fb-b3b4-60d93afd7c6f">Cluster Resource Management Functions</a>



<a href="https://msdn.microsoft.com/49407b45-2b7f-43a2-90ff-98cc557edb31">ClusterResourceCloseEnum</a>



<a href="https://msdn.microsoft.com/f801401f-f49d-41de-b88b-b832330eeccf">ClusterResourceOpenEnum</a>
 

 

