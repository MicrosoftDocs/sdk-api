---
UID: NC:clusapi.PCLUSAPI_SET_GROUP_DEPENDENCY_EXPRESSION
title: PCLUSAPI_SET_GROUP_DEPENDENCY_EXPRESSION
author: windows-sdk-content
description: Sets the dependency expression for a cluster group.
old-location: mscs\setgroupdependencyexpression.htm
old-project: mscs
ms.assetid: 4cf98bed-77fd-4c6a-98c1-ce602e1895f9
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PCLUSAPI_SET_GROUP_DEPENDENCY_EXPRESSION, PCLUSAPI_SET_GROUP_DEPENDENCY_EXPRESSION callback, PCLUSAPI_SET_GROUP_DEPENDENCY_EXPRESSION callback function [Failover Cluster], clusapi/PCLUSAPI_SET_GROUP_DEPENDENCY_EXPRESSION, mscs.setgroupdependencyexpression
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: Sources
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ClusAPI.h
api_name:
 - PCLUSAPI_SET_GROUP_DEPENDENCY_EXPRESSION
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



