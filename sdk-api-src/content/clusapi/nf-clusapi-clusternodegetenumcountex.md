---
UID: NF:clusapi.ClusterNodeGetEnumCountEx
title: ClusterNodeGetEnumCountEx function (clusapi.h)
description: Returns the number of cluster objects that are associated with a node enumeration handle.
helpviewer_keywords: ["ClusterNodeGetEnumCountEx","ClusterNodeGetEnumCountEx function [Failover Cluster]","PCLUSAPI_CLUSTER_NODE_GET_ENUM_COUNT_EX","PCLUSAPI_CLUSTER_NODE_GET_ENUM_COUNT_EX function [Failover Cluster]","clusapi/ClusterNodeGetEnumCountEx","clusapi/PCLUSAPI_CLUSTER_NODE_GET_ENUM_COUNT_EX","mscs.clusternodegetenumcountex"]
old-location: mscs\clusternodegetenumcountex.htm
tech.root: MsCS
ms.assetid: 5C45ED88-9CB4-4C20-97D1-6F02A51048CE
ms.date: 12/05/2018
ms.keywords: ClusterNodeGetEnumCountEx, ClusterNodeGetEnumCountEx function [Failover Cluster], PCLUSAPI_CLUSTER_NODE_GET_ENUM_COUNT_EX, PCLUSAPI_CLUSTER_NODE_GET_ENUM_COUNT_EX function [Failover Cluster], clusapi/ClusterNodeGetEnumCountEx, clusapi/PCLUSAPI_CLUSTER_NODE_GET_ENUM_COUNT_EX, mscs.clusternodegetenumcountex
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 Datacenter, Windows Server 2008 R2 Enterprise
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
 - ClusterNodeGetEnumCountEx
 - clusapi/ClusterNodeGetEnumCountEx
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
 - ClusterNodeGetEnumCountEx
---

# ClusterNodeGetEnumCountEx function


## -description

Returns the number of 
cluster objects that are associated with a 
node enumeration handle.

## -parameters

### -param hNodeEnum [in]

The handle to a node enumeration that was retrieved by the   <a href="/windows/desktop/api/clusapi/nf-clusapi-clusternodeopenenumex">ClusterNodeOpenEnumEx</a> function. A valid handle is required. This parameter cannot be <b>NULL</b>.

## -returns

The number of objects that are associated with the enumeration handle.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/node-management-functions">Node Management Functions</a>