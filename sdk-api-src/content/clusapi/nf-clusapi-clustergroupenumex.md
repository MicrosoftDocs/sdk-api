---
UID: NF:clusapi.ClusterGroupEnumEx
title: ClusterGroupEnumEx function
author: windows-sdk-content
description: Retrieves an item in the enumeration.
old-location: mscs\clustergroupenumex.htm
old-project: mscs
ms.assetid: 139FE5AB-9465-46F8-B360-F27F19D82A88
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusterGroupEnumEx, ClusterGroupEnumEx function [Failover Cluster], PCLUSAPI_CLUSTER_GROUP_ENUM_EX, PCLUSAPI_CLUSTER_GROUP_ENUM_EX function [Failover Cluster], clusapi/ClusterGroupEnumEx, clusapi/PCLUSAPI_CLUSTER_GROUP_ENUM_EX, mscs.clustergroupenumex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.redist: 
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
req.typenames: SR_REPLICATED_DISK_TYPE, *PSR_REPLICATED_DISK_TYPE
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
 - ClusterGroupEnumEx
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# ClusterGroupEnumEx function


## -description


Retrieves an item in the enumeration.The <b>PCLUSAPI_CLUSTER_GROUP_ENUM_EX</b> type defines a pointer to this function.


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



The <b>ClusterGroupEnumEx</b> function doesn't connect to the cluster, because the <i>hGroupEnumEx</i> already contains the enumeration data.  The data is copied into the buffer but no data is retrieved from the cluster.



