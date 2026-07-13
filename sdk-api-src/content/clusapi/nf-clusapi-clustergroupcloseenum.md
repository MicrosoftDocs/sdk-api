---
UID: NF:clusapi.ClusterGroupCloseEnum
title: ClusterGroupCloseEnum function (clusapi.h)
description: Closes a group enumeration handle.
helpviewer_keywords: ["ClusterGroupCloseEnum","ClusterGroupCloseEnum function [Failover Cluster]","PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM","PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM function [Failover Cluster]","_wolf_clustergroupcloseenum","clusapi/ClusterGroupCloseEnum","clusapi/PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM","mscs.clustergroupcloseenum"]
old-location: mscs\clustergroupcloseenum.htm
tech.root: MsCS
ms.assetid: 9bdab6b9-a54d-4166-988c-effdeb2ab254
ms.date: 12/05/2018
ms.keywords: ClusterGroupCloseEnum, ClusterGroupCloseEnum function [Failover Cluster], PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM, PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM function [Failover Cluster], _wolf_clustergroupcloseenum, clusapi/ClusterGroupCloseEnum, clusapi/PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM, mscs.clustergroupcloseenum
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
 - ClusterGroupCloseEnum
 - clusapi/ClusterGroupCloseEnum
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
 - ClusAPI.dll
api_name:
 - ClusterGroupCloseEnum
---

# ClusterGroupCloseEnum function


## -description

Closes a  <a href="/previous-versions/windows/desktop/mscs/groups">group</a> enumeration handle. The <b>PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM</b> type defines a pointer to this function.

## -parameters

### -param hGroupEnum [in]

Enumeration handle to close.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-clustergroupenum">ClusterGroupEnum</a>



<a href="/windows/win32/api/clusapi/nf-clusapi-clustergroupopenenum">ClusterGroupOpenEnum</a>