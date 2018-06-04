---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# PCLUSAPI_GET_CLUSTER_RESOURCE_DEPENDENCY_EXPRESSION callback function


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
 

 

