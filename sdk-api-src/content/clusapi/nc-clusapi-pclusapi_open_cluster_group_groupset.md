---
UID: NC:clusapi.PCLUSAPI_OPEN_CLUSTER_GROUP_GROUPSET
title: PCLUSAPI_OPEN_CLUSTER_GROUP_GROUPSET
author: windows-sdk-content
description: Opens a handle to the specified groupset.
old-location: mscs\openclustergroupcollection.htm
old-project: MsCS
ms.assetid: 8a5b944b-53c2-4437-b580-6ad603d0011a
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PCLUSAPI_OPEN_CLUSTER_GROUP_GROUPSET, PCLUSAPI_OPEN_CLUSTER_GROUP_GROUPSET callback, PCLUSAPI_OPEN_CLUSTER_GROUP_GROUPSET callback function [Failover Cluster], clusapi/PCLUSAPI_OPEN_CLUSTER_GROUP_GROUPSET, mscs.openclustergroupcollection
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
-	PCLUSAPI_OPEN_CLUSTER_GROUP_GROUPSET
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_OPEN_CLUSTER_GROUP_GROUPSET callback function


## -description


Opens a handle to the specified groupset.


## -parameters




### -param hCluster [in]

A handle to the cluster containing the collection.


### -param lpszGroupSetName [in]

The name of the collection to be opened


## -returns



If the operation succeeds, 
the function returns a groupset handle.

If the operation fails, 
the function returns <b>NULL</b>. For more information about the error, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



