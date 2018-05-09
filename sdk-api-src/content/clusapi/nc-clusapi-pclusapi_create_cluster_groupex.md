---
UID: NC:clusapi.PCLUSAPI_CREATE_CLUSTER_GROUPEX
title: PCLUSAPI_CREATE_CLUSTER_GROUPEX
author: windows-driver-content
description: Creates a new cluster group with the options specified in the CLUSTER_CREATE_GROUP_INFO structure in a single operation.
old-location: mscs\createclustergroupex.htm
old-project: MsCS
ms.assetid: D24A2622-758D-4344-8872-F0D8E4EE80CC
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: PCLUSAPI_CREATE_CLUSTER_GROUPEX, PCLUSAPI_CREATE_CLUSTER_GROUPEX callback, PCLUSAPI_CREATE_CLUSTER_GROUPEX callback function [Failover Cluster], clusapi/PCLUSAPI_CREATE_CLUSTER_GROUPEX, mscs.createclustergroupex
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
-	PCLUSAPI_CREATE_CLUSTER_GROUPEX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CREATE_CLUSTER_GROUPEX callback function


## -description


Creates a new cluster group with the options specified in the <b>CLUSTER_CREATE_GROUP_INFO</b> structure in a single operation.
   The <b>PCLUSAPI_CREATE_CLUSTER_GROUPEX</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

The handle to the cluster in which the group will be created.


### -param lpszGroupName [in]

The name of the new cluster group.


### -param pGroupInfo [in, optional]

The additional information used to create the group.


## -returns



If the operation is successful, the function returns a handle to the newly created group.
If the operation fails, the function returns <b>NULL</b>.




## -remarks



The <b>CLUSTER_CREATE_GROUP_INFO</b> structure enables additional properties for group creation.  Currently, only the group type can be specified, which  enables the group type to be set when the group is created.



