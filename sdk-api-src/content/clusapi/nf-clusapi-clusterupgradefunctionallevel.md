---
UID: NF:clusapi.ClusterUpgradeFunctionalLevel
title: ClusterUpgradeFunctionalLevel function
author: windows-sdk-content
description: Initiates a rolling upgrade of the operating system on a cluster. PCLUSAPI_CLUSTER_UPGRADE defines a pointer to this function.
old-location: mscs\clusterupgradefunctionallevel.htm
tech.root: mscs
ms.assetid: EA013501-A4E2-48D8-9062-D20141485CC5
ms.author: windowssdkdev
ms.date: 11/06/2018
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

A pointer to the <a href="https://msdn.microsoft.com/EE803D8C-3EFD-414F-8E38-65A1DFA8079B">ClusterUpgradeProgressCallback</a> callback function that retrieves the status of the rolling upgrade.


### -param pvCallbackArg [in, optional]

A pointer to the arguments for <b>pfnProgressCallback</b>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>. If the operation fails, the function returns a system error code.




## -see-also




<a href="https://msdn.microsoft.com/55E9FF3F-B4B7-4A94-A515-D608A37DF84E">ClusterFunctionalLevel</a>



<a href="https://msdn.microsoft.com/1b3a3b23-39db-47b7-b4a8-17fc1ee45df6">Failover Cluster Management Functions</a>
 

 

