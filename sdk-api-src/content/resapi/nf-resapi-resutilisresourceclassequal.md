---
UID: NF:resapi.ResUtilIsResourceClassEqual
title: ResUtilIsResourceClassEqual function (resapi.h)
description: Tests whether the resource class of a specified resource is equal to a specified resource class. The PRESUTIL_IS_RESOURCE_CLASS_EQUAL type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_IS_RESOURCE_CLASS_EQUAL","PRESUTIL_IS_RESOURCE_CLASS_EQUAL function [Failover Cluster]","ResUtilIsResourceClassEqual","ResUtilIsResourceClassEqual function [Failover Cluster]","_wolf_resutilisresourceclassequal","mscs.resutilisresourceclassequal","resapi/PRESUTIL_IS_RESOURCE_CLASS_EQUAL","resapi/ResUtilIsResourceClassEqual"]
old-location: mscs\resutilisresourceclassequal.htm
tech.root: MsCS
ms.assetid: 3200abd3-5f95-48c5-acd9-8094c0072039
ms.date: 12/05/2018
ms.keywords: PRESUTIL_IS_RESOURCE_CLASS_EQUAL, PRESUTIL_IS_RESOURCE_CLASS_EQUAL function [Failover Cluster], ResUtilIsResourceClassEqual, ResUtilIsResourceClassEqual function [Failover Cluster], _wolf_resutilisresourceclassequal, mscs.resutilisresourceclassequal, resapi/PRESUTIL_IS_RESOURCE_CLASS_EQUAL, resapi/ResUtilIsResourceClassEqual
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
 - ResUtilIsResourceClassEqual
 - resapi/ResUtilIsResourceClassEqual
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilIsResourceClassEqual
---

# ResUtilIsResourceClassEqual function


## -description

Tests whether the resource class of a specified  <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> is equal to a specified resource class. The <b>PRESUTIL_IS_RESOURCE_CLASS_EQUAL</b> type defines a pointer to this function.

## -parameters

### -param prci [in]

Pointer to a  <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_resource_class_info">CLUS_RESOURCE_CLASS_INFO</a> structure describing the resource class.

### -param hResource [in]

Handle to the resource whose class is to be compared to <i>prci</i>.

## -returns

If the resource classes are equal, the function returns <b>TRUE</b>.

If the resource classes are not equal, 
the function returns <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/resapi/nf-resapi-resutilresourcesequal">ResUtilResourcesEqual</a>