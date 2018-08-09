---
UID: NF:clusapi.AddClusterGroupDependency
title: AddClusterGroupDependency function
author: windows-sdk-content
description: Adds a dependency between two cluster groups.
old-location: mscs\addclustergroupdependency.htm
old-project: mscs
ms.assetid: 595921d5-cca0-49fc-b1f5-55af2c73ed74
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AddClusterGroupDependency, AddClusterGroupDependency function [Failover Cluster], PCLUSAPI_ADD_CLUSTER_GROUP_DEPENDENCY, PCLUSAPI_ADD_CLUSTER_GROUP_DEPENDENCY function [Failover Cluster], clusapi/AddClusterGroupDependency, clusapi/PCLUSAPI_ADD_CLUSTER_GROUP_DEPENDENCY, mscs.addclustergroupdependency
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
 - AddClusterGroupDependency
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# AddClusterGroupDependency function


## -description


Adds a dependency between two cluster groups.


## -parameters




### -param hDependentGroup [in]

The dependent group


### -param hProviderGroup [in]

The group <i>hDependentGroup</i> depends on


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.



