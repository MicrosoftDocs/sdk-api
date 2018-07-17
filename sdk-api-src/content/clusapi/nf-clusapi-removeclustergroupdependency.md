---
UID: NF:clusapi.RemoveClusterGroupDependency
title: RemoveClusterGroupDependency function
author: windows-sdk-content
description: Removes a dependency between two cluster groups.
old-location: mscs\removeclustergroupdependency.htm
old-project: mscs
ms.assetid: da264d42-28ee-4589-a790-51da9f788ee9
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: PCLUSAPI_REMOVE_CLUSTER_GROUP_DEPENDENCY, PCLUSAPI_REMOVE_CLUSTER_GROUP_DEPENDENCY function [Failover Cluster], RemoveClusterGroupDependency, RemoveClusterGroupDependency function [Failover Cluster], clusapi/PCLUSAPI_REMOVE_CLUSTER_GROUP_DEPENDENCY, clusapi/RemoveClusterGroupDependency, mscs.removeclustergroupdependency
ms.prod: windows
ms.technology: windows-sdk
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
 - RemoveClusterGroupDependency
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# RemoveClusterGroupDependency function


## -description


Removes a dependency between two cluster groups.


## -parameters




### -param hGroup [in]

The dependent group


### -param hDependsOn [in]

The group <i>hDependentGroup</i> depends on


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.



