---
UID: NF:resapi.ResUtilResourceTypesEqual
title: ResUtilResourceTypesEqual function (resapi.h)
description: Tests whether a resource type matches the resource type name of a specified resource. The PRESUTIL_RESOURCE_TYPES_EQUAL type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_RESOURCE_TYPES_EQUAL","PRESUTIL_RESOURCE_TYPES_EQUAL function [Failover Cluster]","ResUtilResourceTypesEqual","ResUtilResourceTypesEqual function [Failover Cluster]","_wolf_resutilresourcetypesequal","mscs.resutilresourcetypesequal","resapi/PRESUTIL_RESOURCE_TYPES_EQUAL","resapi/ResUtilResourceTypesEqual"]
old-location: mscs\resutilresourcetypesequal.htm
tech.root: MsCS
ms.assetid: 716d2174-5fa7-4868-9f33-ab6f815e6335
ms.date: 12/05/2018
ms.keywords: PRESUTIL_RESOURCE_TYPES_EQUAL, PRESUTIL_RESOURCE_TYPES_EQUAL function [Failover Cluster], ResUtilResourceTypesEqual, ResUtilResourceTypesEqual function [Failover Cluster], _wolf_resutilresourcetypesequal, mscs.resutilresourcetypesequal, resapi/PRESUTIL_RESOURCE_TYPES_EQUAL, resapi/ResUtilResourceTypesEqual
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
 - ResUtilResourceTypesEqual
 - resapi/ResUtilResourceTypesEqual
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
 - ResUtilResourceTypesEqual
---

# ResUtilResourceTypesEqual function


## -description

Tests whether a  <a href="/previous-versions/windows/desktop/mscs/resource-types">resource type</a> matches the resource type name of a specified  <a href="/previous-versions/windows/desktop/mscs/resources">resource</a>. The <b>PRESUTIL_RESOURCE_TYPES_EQUAL</b> type defines a pointer to this function.

## -parameters

### -param lpszResourceTypeName [in]

Pointer to the resource type name to test.

### -param hResource [in]

Handle of the resource to test.

## -returns

If the resource types are equal, the function returns <b>TRUE</b>.

If the resource types are not equal, 
the function returns <b>FALSE</b>.

## -remarks

The  <b>ResUtilResourceTypesEqual</b> utility function compares the resource type name pointed to by <i>lpszResourceTypeName</i> with the resource type name of the resource identified by <i>hResource</i>. To perform the comparison,  <b>ResUtilResourceTypesEqual</b> passes the  <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-get-resource-type">CLUSCTL_RESOURCE_GET_RESOURCE_TYPE</a> control code to the  <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcecontrol">ClusterResourceControl</a> function to retrieve the resource type. If the two resource type names are the same, the resource types are equal. Note that  <b>ResUtilResourceTypesEqual</b> compares the resource type name and not the resource type  <a href="/previous-versions/windows/desktop/mscs/display-names">display name</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-get-resource-type">CLUSCTL_RESOURCE_GET_RESOURCE_TYPE</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcecontrol">ClusterResourceControl</a>