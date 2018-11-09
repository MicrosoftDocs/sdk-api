---
UID: NF:clusapi.GetClusterFromNetInterface
title: GetClusterFromNetInterface function
author: windows-sdk-content
description: Returns a handle to the cluster associated with a network interface.
old-location: mscs\getclusterfromnetinterface.htm
tech.root: mscs
ms.assetid: 7c6c6883-0d88-4162-a70d-cb6f1153226e
ms.author: windowssdkdev
ms.date: 11/06/2018
ms.keywords: GetClusterFromNetInterface, GetClusterFromNetInterface function [Failover Cluster], PCLUSAPI_GET_CLUSTER_FROM_NET_INTERFACE, PCLUSAPI_GET_CLUSTER_FROM_NET_INTERFACE function [Failover Cluster], _wolf_getclusterfromnetinterface, clusapi/GetClusterFromNetInterface, clusapi/PCLUSAPI_GET_CLUSTER_FROM_NET_INTERFACE, mscs.getclusterfromnetinterface
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
 - GetClusterFromNetInterface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetClusterFromNetInterface function


## -description


Returns a handle to the <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a> associated with a  <a href="https://msdn.microsoft.com/en-us/library/Aa371519(v=VS.85).aspx">network interface</a>. The <b>PCLUSAPI_GET_CLUSTER_FROM_NET_INTERFACE</b> type defines a pointer to this function.


## -parameters




### -param hNetInterface [in]

Handle to the network interface.


## -returns



If the operation succeeds, the function returns a handle to the cluster that owns the network interface.

If the operation fails, 
the function returns <b>NULL</b>. For more information about the error, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



For <i>hNetInterface</i> to be a valid handle, there must necessarily be an open cluster handle (see  <a href="https://msdn.microsoft.com/1198ad57-ea47-428f-8867-061afbfc7709">OpenClusterNetInterface</a>).  <b>GetClusterFromNetInterface</b> returns another instance of the handle from which <i>hNetInterface</i> was obtained.

Be sure to call  <a href="https://msdn.microsoft.com/cf055fd6-b1e1-4262-b205-c7d926522450">CloseCluster</a> on the handle returned from  <b>GetClusterFromNetInterface</b> before the handle goes out of scope. Closing this handle does not invalidate <i>hNetInterface</i> or the cluster handle from which <i>hNetInterface</i> was obtained.




## -see-also




<a href="https://msdn.microsoft.com/cf055fd6-b1e1-4262-b205-c7d926522450">CloseCluster</a>



<a href="https://msdn.microsoft.com/e5978e81-790a-4ca7-92b7-d19af31f222e">CloseClusterNetInterface</a>



<a href="https://msdn.microsoft.com/43e1a74f-3320-4b1a-a946-6485d380dda1">GetClusterFromGroup</a>



<a href="https://msdn.microsoft.com/90ac313a-9f60-4591-b0fa-89d99b007280">GetClusterFromNetwork</a>



<a href="https://msdn.microsoft.com/8cc0f881-fbf2-452c-a044-58939f4e01ea">GetClusterFromNode</a>



<a href="https://msdn.microsoft.com/d0ba93cb-94aa-4c68-b87e-518ee1e5c35c">GetClusterFromResource</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>



<a href="https://msdn.microsoft.com/1198ad57-ea47-428f-8867-061afbfc7709">OpenClusterNetInterface</a>
 

 

