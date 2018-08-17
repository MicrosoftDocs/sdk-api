---
UID: NC:clusapi.PCLUSAPI_DESTROY_CLUSTER
title: PCLUSAPI_DESTROY_CLUSTER
author: windows-sdk-content
description: Removes a cluster.
old-location: mscs\destroycluster.htm
old-project: mscs
ms.assetid: 55e601de-b427-43cd-b7f8-6cc576077e59
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PCLUSAPI_DESTROY_CLUSTER, PCLUSAPI_DESTROY_CLUSTER callback, PCLUSAPI_DESTROY_CLUSTER callback function [Failover Cluster], clusapi/PCLUSAPI_DESTROY_CLUSTER, mscs.destroycluster
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: Sources
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ClusAPI.h
api_name:
 - PCLUSAPI_DESTROY_CLUSTER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_DESTROY_CLUSTER callback function


## -description


Removes a cluster. The <b>PCLUSAPI_DESTROY_CLUSTER</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to a cluster, returned by the <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a> or 
      <a href="https://msdn.microsoft.com/672a1573-63e5-4321-a049-25bdafc1b5e0">CreateCluster</a> function.


### -param pfnProgressCallback [in, optional]

Address of callback function that matches the 
      <a href="https://msdn.microsoft.com/en-us/library/Bb394687(v=VS.85).aspx">PCLUSTER_SETUP_PROGRESS_CALLBACK</a> 
      function pointer that will be called periodically to provide progress on the cluster destruction.


### -param pvCallbackArg [in, optional]

Argument for the callback function.


### -param fdeleteVirtualComputerObjects [in]

If <b>TRUE</b>, then delete the virtual computer objects associated with the cluster 
      from the directory.


## -returns



Returns <b>ERROR_SUCCESS</b> if the cluster was completely removed or a 
      <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a> for the last failed operation.




## -remarks



It is possible for multiple steps to fail when removing a cluster with 
    <i>DestroyCluster</i>, but only one error code can be 
    returned. The cluster error log should be reviewed if an error is returned.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa369107(v=VS.85).aspx">Cluster Management Functions</a>



<a href="https://msdn.microsoft.com/672a1573-63e5-4321-a049-25bdafc1b5e0">CreateCluster</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>
 

 

