---
UID: NC:clusapi.PCLUSAPI_CLUSTER_ADD_GROUP_TO_GROUP_GROUPSET
title: PCLUSAPI_CLUSTER_ADD_GROUP_TO_GROUP_GROUPSET
author: windows-sdk-content
description: Adds the specified group to a groupset in the cluster.
old-location: mscs\clusteraddgrouptogroupcollection.htm
old-project: MsCS
ms.assetid: f201dfaa-d9e6-41e0-8d22-23c073b1789d
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PCLUSAPI_CLUSTER_ADD_GROUP_TO_GROUP_GROUPSET, PCLUSAPI_CLUSTER_ADD_GROUP_TO_GROUP_GROUPSET callback, PCLUSAPI_CLUSTER_ADD_GROUP_TO_GROUP_GROUPSET callback function [Failover Cluster], clusapi/PCLUSAPI_CLUSTER_ADD_GROUP_TO_GROUP_GROUPSET, mscs.clusteraddgrouptogroupcollection
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
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_CLUSTER_ADD_GROUP_TO_GROUP_GROUPSET
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLUSTER_ADD_GROUP_TO_GROUP_GROUPSET callback function


## -description


Adds the specified group to a groupset in the cluster. The group
    must not currently be in a groupset


## -parameters




### -param hGroupSet [in]

The collection to which to add the group


### -param hGroup [in]

The group to add to the collection


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.



