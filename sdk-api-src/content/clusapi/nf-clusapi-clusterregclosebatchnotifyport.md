---
UID: NF:clusapi.ClusterRegCloseBatchNotifyPort
title: ClusterRegCloseBatchNotifyPort function
author: windows-sdk-content
description: Closes a subscription to a batch notification port created by the ClusterRegCreateBatchNotifyPort function.
old-location: mscs\clusterregclosebatchnotifyport.htm
tech.root: mscs
ms.assetid: 7ae10343-c97e-4036-9fe6-b894394bb605
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ClusterRegCloseBatchNotifyPort, ClusterRegCloseBatchNotifyPort function [Failover Cluster], PCLUSTER_REG_CLOSE_BATCH_NOTIFY_PORT, clusapi/ClusterRegCloseBatchNotifyPort, mscs.clusterregclosebatchnotifyport
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
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
api_name:
 - ClusterRegCloseBatchNotifyPort
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterRegCloseBatchNotifyPort function


## -description


Closes a subscription to a batch notification port created by the 
    <a href="https://msdn.microsoft.com/1eca2ba5-c0c3-4388-9384-db9dbcfc8405">ClusterRegCreateBatchNotifyPort</a> 
    function.


## -parameters




### -param hBatchNotifyPort [in]

A handle to the batch notification port created earlier via the 
       <a href="https://msdn.microsoft.com/1eca2ba5-c0c3-4388-9384-db9dbcfc8405">ClusterRegCreateBatchNotifyPort</a> 
       function.


## -returns



The function returns one of the following 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.

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
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The handle is not valid.

</td>
</tr>
</table>
 




## -remarks



The <b>PCLUSTER_REG_CLOSE_BATCH_NOTIFY_PORT</b> type defines a pointer to this 
     function.




## -see-also




<a href="https://msdn.microsoft.com/2bb0650f-ef9c-40bb-ae90-229bfa23838e">Cluster Registry Access Functions</a>



<a href="https://msdn.microsoft.com/1eca2ba5-c0c3-4388-9384-db9dbcfc8405">ClusterRegCreateBatchNotifyPort</a>
 

 

