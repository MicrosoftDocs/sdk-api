---
UID: NF:clusapi.GetClusterResourceDependencyExpression
title: GetClusterResourceDependencyExpression function (clusapi.h)
description: Retrieves the dependency expression associated with the specified resource.
helpviewer_keywords: ["GetClusterResourceDependencyExpression","GetClusterResourceDependencyExpression function [Failover Cluster]","PCLUSAPI_GET_CLUSTER_RESOURCE_DEPENDENCY_EXPRESSION","PCLUSAPI_GET_CLUSTER_RESOURCE_DEPENDENCY_EXPRESSION function [Failover Cluster]","clusapi/GetClusterResourceDependencyExpression","clusapi/PCLUSAPI_GET_CLUSTER_RESOURCE_DEPENDENCY_EXPRESSION","mscs.getclusterresourcedependencyexpression"]
old-location: mscs\getclusterresourcedependencyexpression.htm
tech.root: MsCS
ms.assetid: 16071086-66fe-428e-9bd5-dd0b31cf7b15
ms.date: 12/05/2018
ms.keywords: GetClusterResourceDependencyExpression, GetClusterResourceDependencyExpression function [Failover Cluster], PCLUSAPI_GET_CLUSTER_RESOURCE_DEPENDENCY_EXPRESSION, PCLUSAPI_GET_CLUSTER_RESOURCE_DEPENDENCY_EXPRESSION function [Failover Cluster], clusapi/GetClusterResourceDependencyExpression, clusapi/PCLUSAPI_GET_CLUSTER_RESOURCE_DEPENDENCY_EXPRESSION, mscs.getclusterresourcedependencyexpression
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetClusterResourceDependencyExpression
 - clusapi/GetClusterResourceDependencyExpression
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
 - GetClusterResourceDependencyExpression
---

# GetClusterResourceDependencyExpression function


## -description

Retrieves the dependency expression associated with the specified resource. The <b>PCLUSAPI_GET_CLUSTER_RESOURCE_DEPENDENCY_EXPRESSION</b> type defines a pointer to this function.

## -parameters

### -param hResource [in]

Handle to the resource.

### -param lpszDependencyExpression [out, optional]

Address of buffer that will receive the dependency expression.

### -param lpcchDependencyExpression [in, out]

Size in characters of the buffer pointed to by the <i>lpszDependencyExpression</i> 
      parameter.

## -returns

<b>ERROR_SUCCESS</b> (0) if successful.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-management-functions">Failover Cluster Resource Management Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-setclusterresourcedependencyexpression">SetClusterResourceDependencyExpression</a>