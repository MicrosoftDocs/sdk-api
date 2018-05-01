---
UID: NC:clusapi.PCLUSAPI_GET_CLUSTER_RESOURCE_DEPENDENCY_EXPRESSION
title: PCLUSAPI_GET_CLUSTER_RESOURCE_DEPENDENCY_EXPRESSION
author: windows-driver-content
description: Retrieves the dependency expression associated with the specified resource.
old-location: mscs\getclusterresourcedependencyexpression.htm
old-project: MsCS
ms.assetid: 16071086-66fe-428e-9bd5-dd0b31cf7b15
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PCLUSAPI_GET_CLUSTER_RESOURCE_DEPENDENCY_EXPRESSION, PCLUSAPI_GET_CLUSTER_RESOURCE_DEPENDENCY_EXPRESSION callback function [Failover Cluster], clusapi/PCLUSAPI_GET_CLUSTER_RESOURCE_DEPENDENCY_EXPRESSION, mscs.getclusterresourcedependencyexpression
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_GET_CLUSTER_RESOURCE_DEPENDENCY_EXPRESSION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_GET_CLUSTER_RESOURCE_DEPENDENCY_EXPRESSION callback


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




<a href="https://msdn.microsoft.com/d1f7360d-f592-49fb-b3b4-60d93afd7c6f">Failover Cluster Resource Management Functions</a>



<a href="https://msdn.microsoft.com/40f1bff3-1456-4af4-a8fd-8f7998fe60eb">SetClusterResourceDependencyExpression</a>
 

 

