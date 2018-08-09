---
UID: NC:clusapi.PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM_EX
title: PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM_EX
author: windows-sdk-content
description: Closes the enumeration and frees any memory held by the hGroupEnumEx handle.
old-location: mscs\clustergroupcloseenumex.htm
old-project: mscs
ms.assetid: 4777BB89-FB90-43F9-81B4-FCAE4E50889F
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusterGroupCloseEnumEx, ClusterGroupCloseEnumEx function [Failover Cluster], PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM_EX, PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM_EX function [Failover Cluster], clusapi/ClusterGroupCloseEnumEx, clusapi/PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM_EX, mscs.clustergroupcloseenumex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: Sources
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - ClusterGroupCloseEnumEx
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM_EX callback function


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



