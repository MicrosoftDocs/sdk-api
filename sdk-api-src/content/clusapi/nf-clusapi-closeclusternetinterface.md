---
UID: NF:clusapi.CloseClusterNetInterface
title: CloseClusterNetInterface function
author: windows-sdk-content
description: Closes a network interface handle.
old-location: mscs\closeclusternetinterface.htm
tech.root: MsCS
ms.assetid: e5978e81-790a-4ca7-92b7-d19af31f222e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CloseClusterNetInterface, CloseClusterNetInterface function [Failover Cluster], PCLUSAPI_CLOSE_CLUSTER_NET_INTERFACE, PCLUSAPI_CLOSE_CLUSTER_NET_INTERFACE function [Failover Cluster], _wolf_closeclusternetinterface, clusapi/CloseClusterNetInterface, clusapi/PCLUSAPI_CLOSE_CLUSTER_NET_INTERFACE, mscs.closeclusternetinterface
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
api_name:
 - CloseClusterNetInterface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CloseClusterNetInterface
: 
---

# CloseClusterNetInterface function


## -description


Closes a  <a href="https://msdn.microsoft.com/cc0cbbc3-e342-483e-9c94-4ee43f4d588d">network interface</a> handle. The <b>PCLUSAPI_CLOSE_CLUSTER_NET_INTERFACE</b> type defines a pointer to this function.


## -parameters




### -param hNetInterface [in]

Handle of the network interface to close.


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




<a href="https://msdn.microsoft.com/1198ad57-ea47-428f-8867-061afbfc7709">OpenClusterNetInterface</a>
 

 

