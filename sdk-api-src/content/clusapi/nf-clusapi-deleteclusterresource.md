---
UID: NF:clusapi.DeleteClusterResource
title: DeleteClusterResource function
author: windows-sdk-content
description: Removes an offline resource from a cluster.
old-location: mscs\deleteclusterresource.htm
tech.root: MsCS
ms.assetid: d6a8425c-c926-46d8-b13a-c293f8ed30a8
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DeleteClusterResource, DeleteClusterResource function [Failover Cluster], PCLUSAPI_DELETE_CLUSTER_RESOURCE, PCLUSAPI_DELETE_CLUSTER_RESOURCE function [Failover Cluster], _wolf_deleteclusterresource, clusapi/DeleteClusterResource, clusapi/PCLUSAPI_DELETE_CLUSTER_RESOURCE, mscs.deleteclusterresource
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
 - DeleteClusterResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DeleteClusterResource
: 
---

# DeleteClusterResource function


## -description


Removes an offline  <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource</a> from a <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a>. The <b>PCLUSAPI_DELETE_CLUSTER_RESOURCE</b> type defines a pointer to this function.


## -parameters




### -param hResource [in]

Handle to an offline resource. You must close this handle separately.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>, such as one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_RESOURCE_ONLINE</b></dt>
</dl>
</td>
<td width="60%">
Windows Server 2008 R2: The resource identified by <i>hResource</i> is not offline currently.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
Windows Server 2012: The resource identified by <i>hResource</i> is not offline currently.

</td>
</tr>
</table>
 




## -remarks



<b>DeleteClusterResource</b> does not close the resource handle specified by <i>hResource</i>. To avoid memory leaks, be sure to close this handle with  <a href="https://msdn.microsoft.com/dbefd7f9-3499-45b3-a5c8-d0000632f61c">CloseClusterResource</a>.

Do not call  <b>DeleteClusterResource</b> from a resource DLL. For more information, see  <a href="https://msdn.microsoft.com/en-us/library/Aa369588(v=VS.85).aspx">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/dbefd7f9-3499-45b3-a5c8-d0000632f61c">CloseClusterResource</a>



<a href="https://msdn.microsoft.com/c9fe8fa8-57d7-4866-8113-694dc44dae22">CreateClusterResource</a>



<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>
 

 

