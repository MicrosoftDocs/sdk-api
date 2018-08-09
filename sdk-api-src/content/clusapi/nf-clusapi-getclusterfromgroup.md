---
UID: NF:clusapi.GetClusterFromGroup
title: GetClusterFromGroup function
author: windows-sdk-content
description: Returns a handle to the cluster associated with a group.
old-location: mscs\getclusterfromgroup.htm
old-project: mscs
ms.assetid: 43e1a74f-3320-4b1a-a946-6485d380dda1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetClusterFromGroup, GetClusterFromGroup function [Failover Cluster], PCLUSAPI_GET_CLUSTER_FROM_GROUP, PCLUSAPI_GET_CLUSTER_FROM_GROUP function [Failover Cluster], _wolf_getclusterfromgroup, clusapi/GetClusterFromGroup, clusapi/PCLUSAPI_GET_CLUSTER_FROM_GROUP, mscs.getclusterfromgroup
ms.prod: windows
ms.technology: windows-sdk
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
 - GetClusterFromGroup
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# GetClusterFromGroup function


## -description


Returns a handle to the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> associated with a  <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a>. The <b>PCLUSAPI_GET_CLUSTER_FROM_GROUP</b> type defines a pointer to this function.


## -parameters




### -param hGroup [in]

Handle to the group.


## -returns



If the operation succeeds, the function returns a handle to the cluster that owns the group.

If the operation fails, 
the function returns <b>NULL</b>. For more information about the error, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



For <i>hGroup</i> to be a valid handle, there must necessarily be an open cluster handle (see  <a href="https://msdn.microsoft.com/0c7ef9d9-d32b-448e-9e07-6befb9b3e338">OpenClusterGroup</a>).  <b>GetClusterFromGroup</b> returns another instance of the handle from which <i>hGroup</i> was obtained.

Be sure to call  <a href="https://msdn.microsoft.com/cf055fd6-b1e1-4262-b205-c7d926522450">CloseCluster</a> on the handle returned from  <b>GetClusterFromGroup</b> before the handle goes out of scope. Closing this handle does not invalidate <i>hGroup</i> or the cluster handle from which <i>hGroup</i> was obtained.




## -see-also




<a href="https://msdn.microsoft.com/cf055fd6-b1e1-4262-b205-c7d926522450">CloseCluster</a>



<a href="https://msdn.microsoft.com/7c6c6883-0d88-4162-a70d-cb6f1153226e">GetClusterFromNetInterface</a>



<a href="https://msdn.microsoft.com/90ac313a-9f60-4591-b0fa-89d99b007280">GetClusterFromNetwork</a>



<a href="https://msdn.microsoft.com/8cc0f881-fbf2-452c-a044-58939f4e01ea">GetClusterFromNode</a>



<a href="https://msdn.microsoft.com/d0ba93cb-94aa-4c68-b87e-518ee1e5c35c">GetClusterFromResource</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>



<a href="https://msdn.microsoft.com/0c7ef9d9-d32b-448e-9e07-6befb9b3e338">OpenClusterGroup</a>
 

 

