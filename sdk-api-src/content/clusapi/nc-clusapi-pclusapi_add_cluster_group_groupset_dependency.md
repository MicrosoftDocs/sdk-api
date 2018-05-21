---
UID: NC:clusapi.PCLUSAPI_ADD_CLUSTER_GROUP_GROUPSET_DEPENDENCY
title: PCLUSAPI_ADD_CLUSTER_GROUP_GROUPSET_DEPENDENCY
author: windows-driver-content
description: Adds a dependency between two cluster groupsets.
old-location: mscs\addclustergroupcollectiondependency.htm
old-project: MsCS
ms.assetid: dab8cef1-475b-4d92-8f3f-e828d62bcd17
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: PCLUSAPI_ADD_CLUSTER_GROUP_GROUPSET_DEPENDENCY, PCLUSAPI_ADD_CLUSTER_GROUP_GROUPSET_DEPENDENCY callback, PCLUSAPI_ADD_CLUSTER_GROUP_GROUPSET_DEPENDENCY callback function [Failover Cluster], clusapi/PCLUSAPI_ADD_CLUSTER_GROUP_GROUPSET_DEPENDENCY, mscs.addclustergroupcollectiondependency
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
-	PCLUSAPI_ADD_CLUSTER_GROUP_GROUPSET_DEPENDENCY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_ADD_CLUSTER_GROUP_GROUPSET_DEPENDENCY callback function


## -description


Adds a dependency between two cluster groupsets. A groupset can only be dependent
    on one other groupset.


## -parameters




### -param hDependentGroupSet [in]

The dependent collection


### -param hProviderGroupSet [in]

The collection <i>hDependentGroupSet</i> depends on.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.



