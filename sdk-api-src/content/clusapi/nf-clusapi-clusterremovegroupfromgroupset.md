---
UID: NF:clusapi.ClusterRemoveGroupFromGroupSet
title: ClusterRemoveGroupFromGroupSet function (clusapi.h)
author: windows-sdk-content
description: Removes the specified group from the groupset to which it is currently a member.
old-location: mscs\clusterremovegroupfromgroupcollection.htm
tech.root: MsCS
ms.assetid: 26fdf045-0c7d-49ca-adc4-2f687e85b858
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ClusterRemoveGroupFromGroupSet, ClusterRemoveGroupFromGroupSet function [Failover Cluster], PCLUSAPI_CLUSTER_REMOVE_GROUP_FROM_GROUP_GROUPSET, PCLUSAPI_CLUSTER_REMOVE_GROUP_FROM_GROUP_GROUPSET function [Failover Cluster], clusapi/ClusterRemoveGroupFromGroupSet, clusapi/PCLUSAPI_CLUSTER_REMOVE_GROUP_FROM_GROUP_GROUPSET, mscs.clusterremovegroupfromgroupcollection
ms.topic: function
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - ClusterRemoveGroupFromGroupSet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ClusterRemoveGroupFromGroupSet function


## -description


Removes the specified group from the groupset to which it is currently a member.


## -parameters




### -param hGroup [in]

A handle to the group to remove.


## -returns



Returns <b>ERROR_SUCCESS</b>  if successful, or if the group was not currently a member of a collection.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.



