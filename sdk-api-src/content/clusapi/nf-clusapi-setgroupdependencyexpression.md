---
UID: NF:clusapi.SetGroupDependencyExpression
title: SetGroupDependencyExpression function (clusapi.h)
description: Sets the dependency expression for a cluster group.
helpviewer_keywords: ["PCLUSAPI_SET_GROUP_DEPENDENCY_EXPRESSION","PCLUSAPI_SET_GROUP_DEPENDENCY_EXPRESSION function [Failover Cluster]","SetGroupDependencyExpression","SetGroupDependencyExpression function [Failover Cluster]","clusapi/PCLUSAPI_SET_GROUP_DEPENDENCY_EXPRESSION","clusapi/SetGroupDependencyExpression","mscs.setgroupdependencyexpression"]
old-location: mscs\setgroupdependencyexpression.htm
tech.root: MsCS
ms.assetid: 4cf98bed-77fd-4c6a-98c1-ce602e1895f9
ms.date: 12/05/2018
ms.keywords: PCLUSAPI_SET_GROUP_DEPENDENCY_EXPRESSION, PCLUSAPI_SET_GROUP_DEPENDENCY_EXPRESSION function [Failover Cluster], SetGroupDependencyExpression, SetGroupDependencyExpression function [Failover Cluster], clusapi/PCLUSAPI_SET_GROUP_DEPENDENCY_EXPRESSION, clusapi/SetGroupDependencyExpression, mscs.setgroupdependencyexpression
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
 - SetGroupDependencyExpression
 - clusapi/SetGroupDependencyExpression
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
 - SetGroupDependencyExpression
---

# SetGroupDependencyExpression function


## -description

Sets the dependency expression for a cluster group.

## -parameters

### -param hGroup [in]

A handle to the group on which to set the dependency expression.

### -param lpszDependencyExpression [in]

The dependency expression to set on the group.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.