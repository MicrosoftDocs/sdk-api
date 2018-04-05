---
UID: NC:clusapi.PCLUSAPI_REMOVE_CLUSTER_GROUP_DEPENDENCY
title: PCLUSAPI_REMOVE_CLUSTER_GROUP_DEPENDENCY
author: windows-driver-content
description: Removes a dependency between two cluster groups.
old-location: mscs\removeclustergroupdependency.htm
old-project: MsCS
ms.assetid: da264d42-28ee-4589-a790-51da9f788ee9
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: PCLUSAPI_REMOVE_CLUSTER_GROUP_DEPENDENCY, PCLUSAPI_REMOVE_CLUSTER_GROUP_DEPENDENCY callback function [Failover Cluster], clusapi/PCLUSAPI_REMOVE_CLUSTER_GROUP_DEPENDENCY, mscs.removeclustergroupdependency
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
req.typenames: LOG_MANAGEMENT_CALLBACKS, *PLOG_MANAGEMENT_CALLBACKS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	clusapi.h
api_name:
-	PCLUSAPI_REMOVE_CLUSTER_GROUP_DEPENDENCY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_REMOVE_CLUSTER_GROUP_DEPENDENCY callback


## -description


Removes a dependency between two cluster groups.


## -parameters




### -param hGroup [in]

The dependent group


### -param hDependsOn [in]

The group <i>hDependentGroup</i> depends on


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.



