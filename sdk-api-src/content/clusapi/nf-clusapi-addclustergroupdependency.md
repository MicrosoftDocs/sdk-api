---
UID: NF:clusapi.AddClusterGroupDependency
title: AddClusterGroupDependency function (clusapi.h)
description: Adds a dependency between two cluster groups.
helpviewer_keywords: ["AddClusterGroupDependency","AddClusterGroupDependency function [Failover Cluster]","PCLUSAPI_ADD_CLUSTER_GROUP_DEPENDENCY","PCLUSAPI_ADD_CLUSTER_GROUP_DEPENDENCY function [Failover Cluster]","clusapi/AddClusterGroupDependency","clusapi/PCLUSAPI_ADD_CLUSTER_GROUP_DEPENDENCY","mscs.addclustergroupdependency"]
old-location: mscs\addclustergroupdependency.htm
tech.root: MsCS
ms.assetid: 595921d5-cca0-49fc-b1f5-55af2c73ed74
ms.date: 12/05/2018
ms.keywords: AddClusterGroupDependency, AddClusterGroupDependency function [Failover Cluster], PCLUSAPI_ADD_CLUSTER_GROUP_DEPENDENCY, PCLUSAPI_ADD_CLUSTER_GROUP_DEPENDENCY function [Failover Cluster], clusapi/AddClusterGroupDependency, clusapi/PCLUSAPI_ADD_CLUSTER_GROUP_DEPENDENCY, mscs.addclustergroupdependency
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AddClusterGroupDependency
 - clusapi/AddClusterGroupDependency
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - AddClusterGroupDependency
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
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.