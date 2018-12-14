---
UID: NF:clusapi.ClusterRegBatchCloseNotification
title: ClusterRegBatchCloseNotification function
author: windows-sdk-content
description: Frees the memory associated with the batch notification.
old-location: mscs\clusterregbatchclosenotification.htm
tech.root: mscs
ms.assetid: d7a127ba-6e97-46ac-8510-2da355359c50
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ClusterRegBatchCloseNotification, ClusterRegBatchCloseNotification function [Failover Cluster], PCLUSTER_REG_BATCH_CLOSE_NOTIFICATION, clusapi/ClusterRegBatchCloseNotification, mscs.clusterregbatchclosenotification
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ClusterRegBatchCloseNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterRegBatchCloseNotification function


## -description


Frees the memory associated with the batch notification.


## -parameters




### -param hBatchNotification [in]

A handle to the batch notification.


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
The operation was successful. This error returns if the command is properly filled.

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
The handle is not valid. This error is returned if the <i>hBatchNotification</i> 
         parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The <b>PCLUSTER_REG_BATCH_CLOSE_NOTIFICATION</b> type defines a pointer to this 
     function.




## -see-also




<a href="https://msdn.microsoft.com/2bb0650f-ef9c-40bb-ae90-229bfa23838e">Cluster Registry Access Functions</a>
 

 

