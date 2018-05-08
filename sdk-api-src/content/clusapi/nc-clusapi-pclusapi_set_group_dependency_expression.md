---
UID: NC:clusapi.PCLUSAPI_SET_GROUP_DEPENDENCY_EXPRESSION
title: PCLUSAPI_SET_GROUP_DEPENDENCY_EXPRESSION
author: windows-driver-content
description: Sets the dependency expression for a cluster group.
old-location: mscs\setgroupdependencyexpression.htm
old-project: MsCS
ms.assetid: 4cf98bed-77fd-4c6a-98c1-ce602e1895f9
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PCLUSAPI_SET_GROUP_DEPENDENCY_EXPRESSION, PCLUSAPI_SET_GROUP_DEPENDENCY_EXPRESSION callback, PCLUSAPI_SET_GROUP_DEPENDENCY_EXPRESSION callback function [Failover Cluster], clusapi/PCLUSAPI_SET_GROUP_DEPENDENCY_EXPRESSION, mscs.setgroupdependencyexpression
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_SET_GROUP_DEPENDENCY_EXPRESSION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_SET_GROUP_DEPENDENCY_EXPRESSION callback function


## -description


Sets the dependency expression for a cluster group.


## -parameters




### -param hGroupSet


### -param lpszDependencyExpression [in]

The dependency expression to set on the group.


#### - hGroup [in]

A handle to the group on which to set the dependency expression.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.



