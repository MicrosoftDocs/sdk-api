---
UID: NF:clusapi.GetClusterResourceDependencyExpression
title: GetClusterResourceDependencyExpression function
author: windows-sdk-content
description: Retrieves the dependency expression associated with the specified resource.
old-location: mscs\getclusterresourcedependencyexpression.htm
tech.root: MsCS
ms.assetid: 16071086-66fe-428e-9bd5-dd0b31cf7b15
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetClusterResourceDependencyExpression, GetClusterResourceDependencyExpression function [Failover Cluster], PCLUSAPI_GET_CLUSTER_RESOURCE_DEPENDENCY_EXPRESSION, PCLUSAPI_GET_CLUSTER_RESOURCE_DEPENDENCY_EXPRESSION function [Failover Cluster], clusapi/GetClusterResourceDependencyExpression, clusapi/PCLUSAPI_GET_CLUSTER_RESOURCE_DEPENDENCY_EXPRESSION, mscs.getclusterresourcedependencyexpression
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - GetClusterResourceDependencyExpression
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/d1f7360d-f592-49fb-b3b4-60d93afd7c6f">Failover Cluster Resource Management Functions</a>



<a href="https://msdn.microsoft.com/40f1bff3-1456-4af4-a8fd-8f7998fe60eb">SetClusterResourceDependencyExpression</a>
 

 

