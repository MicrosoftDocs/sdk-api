---
UID: NC:clusapi.PCLUSAPI_CREATE_CLUSTER_GROUP_GROUPSET
title: PCLUSAPI_CREATE_CLUSTER_GROUP_GROUPSET
author: windows-sdk-content
description: Adds a groupset to a cluster and returns a handle to the newly added groupset.
old-location: mscs\createclustergroupcollection.htm
old-project: MsCS
ms.assetid: cb0cdf78-c6d6-47b3-bd11-5ab70416131b
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: PCLUSAPI_CREATE_CLUSTER_GROUP_GROUPSET, PCLUSAPI_CREATE_CLUSTER_GROUP_GROUPSET callback, PCLUSAPI_CREATE_CLUSTER_GROUP_GROUPSET callback function [Failover Cluster], clusapi/PCLUSAPI_CREATE_CLUSTER_GROUP_GROUPSET, mscs.createclustergroupcollection
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
 - PCLUSAPI_CREATE_CLUSTER_GROUP_GROUPSET
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CREATE_CLUSTER_GROUP_GROUPSET callback function


## -description


Adds a  groupset to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> and returns a handle to the newly added groupset.


## -parameters




### -param hCluster [in]

A handle to the target cluster.


### -param lpszGroupSetName








#### - groupSetName [in]

Pointer to a null-terminated Unicode string containing the name of the groupset to be added.


## -returns



If the operation succeeds, 
returns a groupset handle.

If the operation fails, 
returns <b>NULL</b>. For more information about the error, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



