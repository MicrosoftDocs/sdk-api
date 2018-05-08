---
UID: NC:clusapi.PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM_EX
title: PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM_EX
author: windows-driver-content
description: Opens a handle to the group enumeration.
old-location: mscs\clustergroupopenenumex.htm
old-project: MsCS
ms.assetid: 1BEF74A2-8230-4698-A3B7-FC2AA495D294
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM_EX, PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM_EX callback, PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM_EX callback function [Failover Cluster], clusapi/PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM_EX, mscs.clustergroupopenenumex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
-	PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM_EX callback function


## -description


Opens a handle to the group enumeration.
   The <b>PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM_EX</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

The handle to the cluster on which the enumeration will be performed.


### -param lpszProperties

A pointer to a list of names of common properties.


### -param cbProperties [in]

The size, in bytes, of the <b>lpszProperties</b> field.


### -param lpszRoProperties

A pointer to a list of names of read-only common properties.


### -param cbRoProperties [in]

The size, in bytes, of the <b>lpszRoProperties</b> field.


### -param dwFlags [in]

Reserved for future use. This value must be 0.


## -returns



If the operation is successful, the function returns a handle to the enumeration.

If the operation fails, the function returns <b>NULL</b>.




## -remarks



The <i>ClusterGroupOpenEnumEx</i> function connects to the cluster service via remote procedure call (RPC) and gathers all of the data to handle the entire enumeration.  After the RPC call completes, the data is maintained locally.  The <b>HGROUPENUMEX</b> handle contains all of the data required to satisfy the enumeration.  Additional calls to <a href="https://msdn.microsoft.com/139FE5AB-9465-46F8-B360-F27F19D82A88">ClusterGroupEnumEx</a>   or <a href="https://msdn.microsoft.com/28FCEC17-78C6-4902-BC4C-832BE3347380">ClusterGroupGetEnumCountEx</a> do not connect to the cluster.



