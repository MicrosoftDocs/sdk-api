---
UID: NC:clusapi.PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM_EX
title: PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM_EX
author: windows-sdk-content
description: Closes the enumeration and frees any memory held by the hGroupEnumEx handle.
old-location: mscs\clustergroupcloseenumex.htm
old-project: MsCS
ms.assetid: 4777BB89-FB90-43F9-81B4-FCAE4E50889F
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM_EX, PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM_EX callback, PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM_EX callback function [Failover Cluster], clusapi/PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM_EX, mscs.clustergroupcloseenumex
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
 - UserDefined
api_location:
 - ClusAPI.h
api_name:
 - PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
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
    <i>ClusterGroupCloseEnumEx</i> function is 
    called.



