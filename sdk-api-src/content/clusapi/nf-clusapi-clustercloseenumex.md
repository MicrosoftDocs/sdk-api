---
UID: NF:clusapi.ClusterCloseEnumEx
title: ClusterCloseEnumEx function (clusapi.h)
description: Closes a handle to an enumeration that was opened by the ClusterOpenEnumEx function.
helpviewer_keywords: ["ClusterCloseEnumEx","ClusterCloseEnumEx function [Failover Cluster]","PCLUSAPI_CLUSTER_CLOSE_ENUM_EX","PCLUSAPI_CLUSTER_CLOSE_ENUM_EX function [Failover Cluster]","clusapi/ClusterCloseEnumEx","clusapi/PCLUSAPI_CLUSTER_CLOSE_ENUM_EX","mscs.clustercloseenumex"]
old-location: mscs\clustercloseenumex.htm
tech.root: MsCS
ms.assetid: B62F1259-C4FF-45FC-9EA1-24CABFE1C0F3
ms.date: 12/05/2018
ms.keywords: ClusterCloseEnumEx, ClusterCloseEnumEx function [Failover Cluster], PCLUSAPI_CLUSTER_CLOSE_ENUM_EX, PCLUSAPI_CLUSTER_CLOSE_ENUM_EX function [Failover Cluster], clusapi/ClusterCloseEnumEx, clusapi/PCLUSAPI_CLUSTER_CLOSE_ENUM_EX, mscs.clustercloseenumex
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
 - ClusterCloseEnumEx
 - clusapi/ClusterCloseEnumEx
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
 - ClusterCloseEnumEx
---

# ClusterCloseEnumEx function


## -description

Closes a handle to an enumeration that was opened by the <a href="/windows/desktop/api/clusapi/nf-clusapi-clusteropenenumex">ClusterOpenEnumEx</a> function.

## -parameters

### -param hClusterEnum [in]

The handle to the cluster enumeration  to close. This is a handle that originally was returned by <a href="/windows/desktop/api/clusapi/nf-clusapi-clusteropenenumex">ClusterOpenEnumEx</a>.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-management-functions">Failover Cluster Management Function</a>