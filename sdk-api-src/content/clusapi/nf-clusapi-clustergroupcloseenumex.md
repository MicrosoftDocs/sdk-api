---
UID: NF:clusapi.ClusterGroupCloseEnumEx
title: ClusterGroupCloseEnumEx function (clusapi.h)
description: Closes the enumeration and frees any memory held by the hGroupEnumEx handle.
helpviewer_keywords: ["ClusterGroupCloseEnumEx","ClusterGroupCloseEnumEx function [Failover Cluster]","PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM_EX","PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM_EX function [Failover Cluster]","clusapi/ClusterGroupCloseEnumEx","clusapi/PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM_EX","mscs.clustergroupcloseenumex"]
old-location: mscs\clustergroupcloseenumex.htm
tech.root: MsCS
ms.assetid: 4777BB89-FB90-43F9-81B4-FCAE4E50889F
ms.date: 12/05/2018
ms.keywords: ClusterGroupCloseEnumEx, ClusterGroupCloseEnumEx function [Failover Cluster], PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM_EX, PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM_EX function [Failover Cluster], clusapi/ClusterGroupCloseEnumEx, clusapi/PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM_EX, mscs.clustergroupcloseenumex
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
 - ClusterGroupCloseEnumEx
 - clusapi/ClusterGroupCloseEnumEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-clusapi-l1-1-6.dll
 - ext-ms-win-cluster-clusapi-l1-1-5.dll
 - ext-ms-win-cluster-clusapi-l1-1-4.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - ClusterGroupCloseEnumEx
---

# ClusterGroupCloseEnumEx function


## -description

Closes the enumeration and frees any memory held by the <i>hGroupEnumEx</i> 
    handle. The <b>PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM_EX</b> type defines a pointer to 
    this function.

## -parameters

### -param hGroupEnumEx [in]

The handle to the enumeration that will be freed.

## -returns

ERROR_SUCCESS is returned when the enumeration handle is freed.

## -remarks

Any additional calls using the <i>hGroupEnumEx</i> will fail.  Do not use the 
    <i>hGroupEnumEx</i> handle after the 
    <b>ClusterGroupCloseEnumEx</b> function is 
    called.

