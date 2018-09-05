---
UID: NF:clusapi.GetClusterFromNetwork
title: GetClusterFromNetwork function
author: windows-sdk-content
description: Returns a handle to the cluster associated with a network.
old-location: mscs\getclusterfromnetwork.htm
old-project: mscs
ms.assetid: 90ac313a-9f60-4591-b0fa-89d99b007280
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetClusterFromNetwork, GetClusterFromNetwork function [Failover Cluster], PCLUSAPI_GET_CLUSTER_FROM_NETWORK, PCLUSAPI_GET_CLUSTER_FROM_NETWORK function [Failover Cluster], _wolf_getclusterfromnetwork, clusapi/GetClusterFromNetwork, clusapi/PCLUSAPI_GET_CLUSTER_FROM_NETWORK, mscs.getclusterfromnetwork
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SR_REPLICATED_DISK_TYPE, *PSR_REPLICATED_DISK_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - GetClusterFromNetwork
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# GetClusterFromNetwork function


## -description


Returns a handle to the <a href="c_gly.htm">cluster</a> associated with a  <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">network</a>. The <b>PCLUSAPI_GET_CLUSTER_FROM_NETWORK</b> type defines a pointer to this function.


## -parameters




### -param hNetwork [in]

Handle to the network.


## -returns



If the operation succeeds, the function returns a handle to the cluster that owns the network.

If the operation fails, 
the function returns <b>NULL</b>. For more information about the error, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



For <i>hNetwork</i> to be a valid handle, there must necessarily be an open cluster handle (see  <a href="https://msdn.microsoft.com/a888ca91-e56f-42bc-81c5-9235c6fd5172">OpenClusterNetwork</a>).  <b>GetClusterFromNetwork</b> returns another instance of the handle from which <i>hNetwork</i> was obtained.

Be sure to call  <a href="https://msdn.microsoft.com/cf055fd6-b1e1-4262-b205-c7d926522450">CloseCluster</a> on the handle returned from  <b>GetClusterFromNetwork</b> before the handle goes out of scope. Closing this handle does not invalidate <i>hNetwork</i> or the cluster handle from which <i>hNetwork</i> was obtained.




## -see-also




<a href="https://msdn.microsoft.com/cf055fd6-b1e1-4262-b205-c7d926522450">CloseCluster</a>



<a href="https://msdn.microsoft.com/2d112729-1306-45ff-8845-43032a55ca1c">CloseClusterNetwork</a>



<a href="https://msdn.microsoft.com/43e1a74f-3320-4b1a-a946-6485d380dda1">GetClusterFromGroup</a>



<a href="https://msdn.microsoft.com/7c6c6883-0d88-4162-a70d-cb6f1153226e">GetClusterFromNetInterface</a>



<a href="https://msdn.microsoft.com/8cc0f881-fbf2-452c-a044-58939f4e01ea">GetClusterFromNode</a>



<a href="https://msdn.microsoft.com/d0ba93cb-94aa-4c68-b87e-518ee1e5c35c">GetClusterFromResource</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>



<a href="https://msdn.microsoft.com/a888ca91-e56f-42bc-81c5-9235c6fd5172">OpenClusterNetwork</a>
 

 

