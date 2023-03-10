---
UID: NF:clusapi.ClusterGroupSetCloseEnum
title: ClusterGroupSetCloseEnum function (clusapi.h)
description: Closes an open enumeration for a groupset.
helpviewer_keywords: ["ClusterGroupSetCloseEnum","ClusterGroupSetCloseEnum function [Failover Cluster]","PCLUSAPI_CLOSE_CLUSTER_GROUP_GROUPSET","PCLUSAPI_CLOSE_CLUSTER_GROUP_GROUPSET function [Failover Cluster]","clusapi/ClusterGroupSetCloseEnum","clusapi/PCLUSAPI_CLOSE_CLUSTER_GROUP_GROUPSET","mscs.clustergroupcollectioncloseenum"]
old-location: mscs\clustergroupcollectioncloseenum.htm
tech.root: MsCS
ms.assetid: b82e13f0-364c-41cf-9fda-98a95f23ff7d
ms.date: 12/05/2018
ms.keywords: ClusterGroupSetCloseEnum, ClusterGroupSetCloseEnum function [Failover Cluster], PCLUSAPI_CLOSE_CLUSTER_GROUP_GROUPSET, PCLUSAPI_CLOSE_CLUSTER_GROUP_GROUPSET function [Failover Cluster], clusapi/ClusterGroupSetCloseEnum, clusapi/PCLUSAPI_CLOSE_CLUSTER_GROUP_GROUPSET, mscs.clustergroupcollectioncloseenum
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ClusterGroupSetCloseEnum
 - clusapi/ClusterGroupSetCloseEnum
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
 - ClusterGroupSetCloseEnum
---

# ClusterGroupSetCloseEnum function


## -description

Closes an open enumeration for a groupset.

## -parameters

### -param hGroupSetEnum [in]

The enumeration to be closed.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.