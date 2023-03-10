---
UID: NF:clusapi.ClusterNodeCloseEnumEx
title: ClusterNodeCloseEnumEx function (clusapi.h)
description: Closes a node enumeration handle. (ClusterNodeCloseEnumEx)
helpviewer_keywords: ["ClusterNodeCloseEnumEx","ClusterNodeCloseEnumEx function [Failover Cluster]","PCLUSAPI_CLUSTER_NODE_CLOSE_ENUM_EX","PCLUSAPI_CLUSTER_NODE_CLOSE_ENUM_EX function [Failover Cluster]","clusapi/ClusterNodeCloseEnumEx","clusapi/PCLUSAPI_CLUSTER_NODE_CLOSE_ENUM_EX","mscs.clusternodecloseenumex"]
old-location: mscs\clusternodecloseenumex.htm
tech.root: MsCS
ms.assetid: 1B743E4E-F8E0-4E73-B5FA-53D4FC547251
ms.date: 12/05/2018
ms.keywords: ClusterNodeCloseEnumEx, ClusterNodeCloseEnumEx function [Failover Cluster], PCLUSAPI_CLUSTER_NODE_CLOSE_ENUM_EX, PCLUSAPI_CLUSTER_NODE_CLOSE_ENUM_EX function [Failover Cluster], clusapi/ClusterNodeCloseEnumEx, clusapi/PCLUSAPI_CLUSTER_NODE_CLOSE_ENUM_EX, mscs.clusternodecloseenumex
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
 - ClusterNodeCloseEnumEx
 - clusapi/ClusterNodeCloseEnumEx
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
 - ClusterNodeCloseEnumEx
---

# ClusterNodeCloseEnumEx function


## -description

Closes a 
node enumeration handle.

## -parameters

### -param hNodeEnum [in]

The handle to the node enumeration  to close. This handle is returned by the  <a href="/windows/desktop/api/clusapi/nf-clusapi-clusternodeopenenumex">ClusterNodeOpenEnumEx</a> function.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.
     If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/node-management-functions">Node Management Functions</a>
