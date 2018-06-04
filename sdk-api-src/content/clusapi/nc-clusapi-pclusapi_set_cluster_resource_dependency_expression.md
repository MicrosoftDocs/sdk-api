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

# PCLUSAPI_SET_CLUSTER_RESOURCE_DEPENDENCY_EXPRESSION callback function


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

<pre class="syntax" xml:space="preserve"><code>expression:
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
    | [resourceName]</code></pre>
This gives us expressions of the general form:<b>( [</b><i>id</i><b>] or [</b><i>id</i><b>] ... ) and ( [</b><i>id</i><b>] or [</b><i>id</i><b>] ... ) and ...</b>

For example: ([a904e1b7-95dd-47f0-9b2e-f1007d92699b] or [ae6fcf48-c42f-4960-a61a-7f1044067668]) and ([c471abc6-e454-482e-8be4-fae084cf799b] or [de976488-82cb-4950-8ce0-1b45e868e058])




## -see-also




<a href="https://msdn.microsoft.com/d1f7360d-f592-49fb-b3b4-60d93afd7c6f">Failover Cluster Resource Management Functions</a>



<a href="https://msdn.microsoft.com/16071086-66fe-428e-9bd5-dd0b31cf7b15">GetClusterResourceDependencyExpression</a>
 

 

