---
UID: NF:clusapi.ClusterGroupGetEnumCountEx
title: ClusterGroupGetEnumCountEx function (clusapi.h)
description: Returns the number of elements in the enumeration.
helpviewer_keywords: ["ClusterGroupGetEnumCountEx","ClusterGroupGetEnumCountEx function [Failover Cluster]","PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT_EX","PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT_EX function [Failover Cluster]","clusapi/ClusterGroupGetEnumCountEx","clusapi/PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT_EX","mscs.clustergroupgetenumcountex"]
old-location: mscs\clustergroupgetenumcountex.htm
tech.root: MsCS
ms.assetid: 28FCEC17-78C6-4902-BC4C-832BE3347380
ms.date: 12/05/2018
ms.keywords: ClusterGroupGetEnumCountEx, ClusterGroupGetEnumCountEx function [Failover Cluster], PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT_EX, PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT_EX function [Failover Cluster], clusapi/ClusterGroupGetEnumCountEx, clusapi/PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT_EX, mscs.clustergroupgetenumcountex
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ClusterGroupGetEnumCountEx
 - clusapi/ClusterGroupGetEnumCountEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - ClusterGroupGetEnumCountEx
---

# ClusterGroupGetEnumCountEx function


## -description

Returns the number of elements in the enumeration.The <b>PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT_EX</b> type defines a pointer to this function.

## -parameters

### -param hGroupEnumEx [in]

The handle to the enumeration from which the number of entries will be returned.

## -returns

The number of items in the enumeration.

## -remarks

The <b>ClusterGroupGetEnumCountEx</b> function doesn't connect to the cluster, because <i>hGroupEnumEx</i> handle already contains the enumeration data.

