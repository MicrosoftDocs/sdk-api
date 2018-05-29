---
UID: NC:clusapi.PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT_EX
title: PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT_EX
author: windows-sdk-content
description: Returns the number of elements in the enumeration.
old-location: mscs\clustergroupgetenumcountex.htm
old-project: MsCS
ms.assetid: 28FCEC17-78C6-4902-BC4C-832BE3347380
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT_EX, PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT_EX callback, PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT_EX callback function [Failover Cluster], clusapi/PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT_EX, mscs.clustergroupgetenumcountex
ms.prod: windows
ms.technology: windows-sdk
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
-	PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT_EX callback function


## -description


Returns the number of elements in the enumeration.
   The <b>PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT_EX</b> type defines a pointer to this function.


## -parameters




### -param hGroupEnumEx [in]

The handle to the enumeration from which the number of entries will be returned.


## -returns



The number of items in the enumeration.




## -remarks



The <i>ClusterGroupGetEnumCountEx</i> function doesn't connect to the cluster, because <i>hGroupEnumEx</i> handle already contains the enumeration data.



