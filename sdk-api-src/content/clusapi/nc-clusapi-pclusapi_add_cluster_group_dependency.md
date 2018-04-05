---
UID: NC:clusapi.PCLUSAPI_ADD_CLUSTER_GROUP_DEPENDENCY
title: PCLUSAPI_ADD_CLUSTER_GROUP_DEPENDENCY
author: windows-driver-content
description: Adds a dependency between two cluster groups.
old-location: mscs\addclustergroupdependency.htm
old-project: MsCS
ms.assetid: 595921d5-cca0-49fc-b1f5-55af2c73ed74
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: PCLUSAPI_ADD_CLUSTER_GROUP_DEPENDENCY, PCLUSAPI_ADD_CLUSTER_GROUP_DEPENDENCY callback function [Failover Cluster], clusapi/PCLUSAPI_ADD_CLUSTER_GROUP_DEPENDENCY, mscs.addclustergroupdependency
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
-	ClusAPI.h
api_name:
-	PCLUSAPI_ADD_CLUSTER_GROUP_DEPENDENCY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_ADD_CLUSTER_GROUP_DEPENDENCY callback


## -description


Adds a dependency between two cluster groups.


## -parameters




### -param hDependentGroup [in]

The dependent group


### -param hProviderGroup [in]

The group <i>hDependentGroup</i> depends on


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.



