---
UID: NF:clusapi.SetClusterResourceDependencyExpression
title: SetClusterResourceDependencyExpression function (clusapi.h)
description: Specifies the dependency expression to be associated with the resource referred to by hResource. Any existing dependency relationships for the resource will be overwritten.
helpviewer_keywords: ["PCLUSAPI_SET_CLUSTER_RESOURCE_DEPENDENCY_EXPRESSION","PCLUSAPI_SET_CLUSTER_RESOURCE_DEPENDENCY_EXPRESSION function [Failover Cluster]","SetClusterResourceDependencyExpression","SetClusterResourceDependencyExpression function [Failover Cluster]","clusapi/PCLUSAPI_SET_CLUSTER_RESOURCE_DEPENDENCY_EXPRESSION","clusapi/SetClusterResourceDependencyExpression","mscs.setclusterresourcedependencyexpression"]
old-location: mscs\setclusterresourcedependencyexpression.htm
tech.root: MsCS
ms.assetid: 40f1bff3-1456-4af4-a8fd-8f7998fe60eb
ms.date: 12/05/2018
ms.keywords: PCLUSAPI_SET_CLUSTER_RESOURCE_DEPENDENCY_EXPRESSION, PCLUSAPI_SET_CLUSTER_RESOURCE_DEPENDENCY_EXPRESSION function [Failover Cluster], SetClusterResourceDependencyExpression, SetClusterResourceDependencyExpression function [Failover Cluster], clusapi/PCLUSAPI_SET_CLUSTER_RESOURCE_DEPENDENCY_EXPRESSION, clusapi/SetClusterResourceDependencyExpression, mscs.setclusterresourcedependencyexpression
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
 - SetClusterResourceDependencyExpression
 - clusapi/SetClusterResourceDependencyExpression
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
 - SetClusterResourceDependencyExpression
---

# SetClusterResourceDependencyExpression function


## -description

Specifies the dependency expression to be associated with the resource referred to by 
    <i>hResource</i>.  Any existing dependency relationships for the resource will be 
    overwritten. The <b>PCLUSAPI_SET_CLUSTER_RESOURCE_DEPENDENCY_EXPRESSION</b> type defines a pointer to this function.

## -parameters

### -param hResource [in]

Handle to the resource.

### -param lpszDependencyExpression [in]

Address of Unicode string containing the dependency expression.

## -returns

<b>ERROR_SUCCESS</b> (0) if successful.

## -remarks

The system only supports groups of <b>OR</b> expressions that are combined by using <b>AND</b>. The dependency expressions are 
    described by this BNF grammar.


``` syntax
expression:
      expression_part
    | expression and expression_part

expression_part:
        resource
    | ( or_expression )

or_expression:
        resource
    | or_expression or resource


resource:
    [resourceID]
    | [resourceName]
```

This gives us expressions of the general form:<b>( [</b><i>id</i><b>] or [</b><i>id</i><b>] ... ) and ( [</b><i>id</i><b>] or [</b><i>id</i><b>] ... ) and ...</b>

For example: ([a904e1b7-95dd-47f0-9b2e-f1007d92699b] or [ae6fcf48-c42f-4960-a61a-7f1044067668]) and ([c471abc6-e454-482e-8be4-fae084cf799b] or [de976488-82cb-4950-8ce0-1b45e868e058])

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-management-functions">Failover Cluster Resource Management Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterresourcedependencyexpression">GetClusterResourceDependencyExpression</a>
