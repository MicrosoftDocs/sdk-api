---
UID: NF:clusapi.SetClusterGroupSetDependencyExpression
title: SetClusterGroupSetDependencyExpression function
author: windows-sdk-content
description: Sets the dependency expression for a cluster groupset.
old-location: mscs\setclustergroupcollectiondependencyexpression.htm
tech.root: MsCS
ms.assetid: 1bde6ef6-a415-4fa2-8618-0304c38d9434
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: PCLUSAPI_SET_CLUSTER_GROUP_GROUPSET_DEPENDENCY_EXPRESSION, PCLUSAPI_SET_CLUSTER_GROUP_GROUPSET_DEPENDENCY_EXPRESSION function [Failover Cluster], SetClusterGroupSetDependencyExpression, SetClusterGroupSetDependencyExpression function [Failover Cluster], clusapi/PCLUSAPI_SET_CLUSTER_GROUP_GROUPSET_DEPENDENCY_EXPRESSION, clusapi/SetClusterGroupSetDependencyExpression, mscs.setclustergroupcollectiondependencyexpression
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
 - SetClusterGroupSetDependencyExpression
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetClusterGroupSetDependencyExpression function


## -description


Sets the dependency expression for a cluster groupset.


## -parameters




### -param hGroupSet [in]

The collection to receive the dependency expression


### -param lpszDependencyExprssion [in]

The dependency expression for <i>hCollection</i>


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.



