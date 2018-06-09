---
UID: NC:clusapi.PCLUSAPI_CLUSTER_GROUP_ENUM_EX
title: PCLUSAPI_CLUSTER_GROUP_ENUM_EX
author: windows-sdk-content
description: Retrieves an item in the enumeration.
old-location: mscs\clustergroupenumex.htm
old-project: MsCS
ms.assetid: 139FE5AB-9465-46F8-B360-F27F19D82A88
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: PCLUSAPI_CLUSTER_GROUP_ENUM_EX, PCLUSAPI_CLUSTER_GROUP_ENUM_EX callback, PCLUSAPI_CLUSTER_GROUP_ENUM_EX callback function [Failover Cluster], clusapi/PCLUSAPI_CLUSTER_GROUP_ENUM_EX, mscs.clustergroupenumex
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
 - PCLUSAPI_CLUSTER_GROUP_ENUM_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLUSTER_GROUP_ENUM_EX callback function


## -description


Retrieves an item in the enumeration.
   The <b>PCLUSAPI_CLUSTER_GROUP_ENUM_EX</b> type defines a pointer to this function.


## -parameters




### -param hGroupEnumEx [in]

The handle to the enumeration from which the item will be retrieved.


### -param dwIndex [in]

The zero-based index of the item in the enumeration.


### -param pItem [in, out]

A pointer to the buffer to be filled.


### -param cbItem [in, out]

On input, the size of <i>pItem</i>.

On output, either the required size in bytes of the buffer if the buffer is too small, or the number of bytes written into the buffer.


## -returns





Returns DWORD that ...






## -remarks



The <i>ClusterGroupEnumEx</i> function doesn't connect to the cluster, because the <i>hGroupEnumEx</i> already contains the enumeration data.  The data is copied into the buffer but no data is retrieved from the cluster.



