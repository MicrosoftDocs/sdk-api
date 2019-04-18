---
UID: NF:clusapi.CloseClusterNetwork
title: CloseClusterNetwork function (clusapi.h)
author: windows-sdk-content
description: Closes a network handle.
old-location: mscs\closeclusternetwork.htm
tech.root: MsCS
ms.assetid: 2d112729-1306-45ff-8845-43032a55ca1c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CloseClusterNetwork, CloseClusterNetwork function [Failover Cluster], PCLUSAPI_CLOSE_CLUSTER_NETWORK, PCLUSAPI_CLOSE_CLUSTER_NETWORK function [Failover Cluster], _wolf_closeclusternetwork, clusapi/CloseClusterNetwork, clusapi/PCLUSAPI_CLOSE_CLUSTER_NETWORK, mscs.closeclusternetwork
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
api_name:
 - CloseClusterNetwork
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CloseClusterNetwork function


## -description


Closes a  <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">network</a> handle. The <b>PCLUSAPI_CLOSE_CLUSTER_NETWORK</b> type defines a pointer to this function.


## -parameters




### -param hNetwork [in]

Handle to the network to close.


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The operation was not successful; call the function  <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> for more information.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a888ca91-e56f-42bc-81c5-9235c6fd5172">OpenClusterNetwork</a>
 

 

