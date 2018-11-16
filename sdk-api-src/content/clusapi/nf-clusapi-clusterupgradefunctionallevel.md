---
UID: NF:clusapi.ClusterUpgradeFunctionalLevel
title: ClusterUpgradeFunctionalLevel function
author: windows-sdk-content
description: Initiates a rolling upgrade of the operating system on a cluster. PCLUSAPI_CLUSTER_UPGRADE defines a pointer to this function.
old-location: mscs\clusterupgradefunctionallevel.htm
tech.root: MsCS
ms.assetid: EA013501-A4E2-48D8-9062-D20141485CC5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ClusterUpgradeFunctionalLevel, ClusterUpgradeFunctionalLevel function [Failover Cluster], PCLUSAPI_CLUSTER_UPGRADE, PCLUSAPI_CLUSTER_UPGRADE function [Failover Cluster], clusapi/ClusterUpgradeFunctionalLevel, clusapi/PCLUSAPI_CLUSTER_UPGRADE, mscs.clusterupgradefunctionallevel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
 - ClusterUpgradeFunctionalLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ClusterUpgradeFunctionalLevel
: 
---

# ClusterUpgradeFunctionalLevel function


## -description


Initiates a rolling upgrade of the operating system on a cluster. <b>PCLUSAPI_CLUSTER_UPGRADE</b> defines a pointer to this function.


## -parameters




### -param hCluster [in]

A handle to the cluster to upgrade.


### -param perform [in]

<b>True</b> to initiate the rolling upgrade; otherwise <b>false</b>.


### -param pfnProgressCallback [in, optional]

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dn806599(v=VS.85).aspx">ClusterUpgradeProgressCallback</a> callback function that retrieves the status of the rolling upgrade.


### -param pvCallbackArg [in, optional]

A pointer to the arguments for <b>pfnProgressCallback</b>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>. If the operation fails, the function returns a system error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn806593(v=VS.85).aspx">ClusterFunctionalLevel</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369107(v=VS.85).aspx">Failover Cluster Management Functions</a>
 

 

