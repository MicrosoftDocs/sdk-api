---
UID: NC:clusapi.PCLUSAPI_CLUSTER_REMOVE_GROUP_FROM_GROUP_GROUPSET
title: PCLUSAPI_CLUSTER_REMOVE_GROUP_FROM_GROUP_GROUPSET
author: windows-driver-content
description: Removes the specified group from the groupset to which it is currently a member.
old-location: mscs\clusterremovegroupfromgroupcollection.htm
old-project: MsCS
ms.assetid: 26fdf045-0c7d-49ca-adc4-2f687e85b858
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PCLUSAPI_CLUSTER_REMOVE_GROUP_FROM_GROUP_GROUPSET, PCLUSAPI_CLUSTER_REMOVE_GROUP_FROM_GROUP_GROUPSET callback function [Failover Cluster], clusapi/PCLUSAPI_CLUSTER_REMOVE_GROUP_FROM_GROUP_GROUPSET, mscs.clusterremovegroupfromgroupcollection
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
-	PCLUSAPI_CLUSTER_REMOVE_GROUP_FROM_GROUP_GROUPSET
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLUSTER_REMOVE_GROUP_FROM_GROUP_GROUPSET callback


## -description


Removes the specified group from the groupset to which it is currently a member.


## -parameters




### -param hGroupSet


### -param hGroupName








#### - hGroup [in]

A handle to the group to remove.


## -returns



Returns <b>ERROR_SUCCESS</b>  if successful, or if the group was not currently a member of a collection.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.



