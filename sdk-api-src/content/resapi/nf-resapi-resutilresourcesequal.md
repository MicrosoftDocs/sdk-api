---
UID: NF:resapi.ResUtilResourcesEqual
title: ResUtilResourcesEqual function (resapi.h)
description: Tests whether two resource handles represent the same resource. The PRESUTIL_RESOURCES_EQUAL type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_RESOURCES_EQUAL","PRESUTIL_RESOURCES_EQUAL function [Failover Cluster]","ResUtilResourcesEqual","ResUtilResourcesEqual function [Failover Cluster]","_wolf_resutilresourcesequal","mscs.resutilresourcesequal","resapi/PRESUTIL_RESOURCES_EQUAL","resapi/ResUtilResourcesEqual"]
old-location: mscs\resutilresourcesequal.htm
tech.root: MsCS
ms.assetid: a34bbe15-f13f-4034-b2f1-fea3e58c579e
ms.date: 12/05/2018
ms.keywords: PRESUTIL_RESOURCES_EQUAL, PRESUTIL_RESOURCES_EQUAL function [Failover Cluster], ResUtilResourcesEqual, ResUtilResourcesEqual function [Failover Cluster], _wolf_resutilresourcesequal, mscs.resutilresourcesequal, resapi/PRESUTIL_RESOURCES_EQUAL, resapi/ResUtilResourcesEqual
req.header: resapi.h
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
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ResUtilResourcesEqual
 - resapi/ResUtilResourcesEqual
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-resutils-l1-1-3.dll
 - ResUtils.dll
api_name:
 - ResUtilResourcesEqual
---

# ResUtilResourcesEqual function


## -description

Tests whether two resource handles represent the same  <a href="/previous-versions/windows/desktop/mscs/resources">resource</a>. The <b>PRESUTIL_RESOURCES_EQUAL</b> type defines a pointer to this function.

## -parameters

### -param hSelf [in]

Handle to one of the resources.

### -param hResource [in]

Handle to the other resource.

## -returns

If the resources are equal, the function returns <b>TRUE</b>.

If the resources are not equal, 
the function returns <b>FALSE</b>.

## -remarks

The  <b>ResUtilResourcesEqual</b> utility function compares the two resources by retrieving their names. To retrieve the names,  <b>ResUtilResourcesEqual</b> passes the  <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-get-name">CLUSCTL_RESOURCE_GET_NAME</a> control code to the  <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcecontrol">ClusterResourceControl</a> function. If the names are the same, the resources are equal.

Do not pass LPC and RPC handles in the same function call. If you do, the call will raise an RPC exception and can result in additional destructive effects. For information on how LPC and RPC handles are created, see  <a href="/previous-versions/windows/desktop/mscs/using-object-handles">Using Object Handles</a> and  <a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-get-name">CLUSCTL_RESOURCE_GET_NAME</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcecontrol">ClusterResourceControl</a>