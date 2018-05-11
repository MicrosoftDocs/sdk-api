---
UID: NC:clusapi.PCLUSAPI_DELETE_CLUSTER_GROUP_GROUPSET
title: PCLUSAPI_DELETE_CLUSTER_GROUP_GROUPSET
author: windows-driver-content
description: Deletes the specified groupset from the cluster.
old-location: mscs\deleteclustergroupcollection.htm
old-project: MsCS
ms.assetid: 8787d61b-7a80-404c-985f-1ad4ba01acf0
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: PCLUSAPI_DELETE_CLUSTER_GROUP_GROUPSET, PCLUSAPI_DELETE_CLUSTER_GROUP_GROUPSET callback, PCLUSAPI_DELETE_CLUSTER_GROUP_GROUPSET callback function [Failover Cluster], clusapi/PCLUSAPI_DELETE_CLUSTER_GROUP_GROUPSET, mscs.deleteclustergroupcollection
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
-	PCLUSAPI_DELETE_CLUSTER_GROUP_GROUPSET
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_DELETE_CLUSTER_GROUP_GROUPSET callback function


## -description


Deletes the specified groupset from the cluster. The groupset
    must contain no groups.


## -parameters




### -param hGroupSet [in]

A handle to the collection to be deleted


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.



