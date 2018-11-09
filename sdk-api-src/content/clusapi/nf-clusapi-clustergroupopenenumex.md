---
UID: NF:clusapi.ClusterGroupOpenEnumEx
title: ClusterGroupOpenEnumEx function
author: windows-sdk-content
description: Opens a handle to the group enumeration.
old-location: mscs\clustergroupopenenumex.htm
tech.root: mscs
ms.assetid: 1BEF74A2-8230-4698-A3B7-FC2AA495D294
ms.author: windowssdkdev
ms.date: 11/06/2018
ms.keywords: ClusterGroupOpenEnumEx, ClusterGroupOpenEnumEx function [Failover Cluster], PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM_EX, PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM_EX function [Failover Cluster], clusapi/ClusterGroupOpenEnumEx, clusapi/PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM_EX, mscs.clustergroupopenenumex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
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
 - ClusterGroupOpenEnumEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterGroupOpenEnumEx function


## -description


Opens a handle to the group enumeration.The <b>PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM_EX</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

The handle to the cluster on which the enumeration will be performed.


### -param lpszProperties

A pointer to a list of names of common properties.


### -param cbProperties [in]

The size, in bytes, of the <b>lpszProperties</b> field.


### -param lpszRoProperties

A pointer to a list of names of read-only common properties.


### -param cbRoProperties [in]

The size, in bytes, of the <b>lpszRoProperties</b> field.


### -param dwFlags [in]

Reserved for future use. This value must be 0.


## -returns



If the operation is successful, the function returns a handle to the enumeration.

If the operation fails, the function returns <b>NULL</b>.




## -remarks



The <b>ClusterGroupOpenEnumEx</b> function connects to the cluster service via remote procedure call (RPC) and gathers all of the data to handle the entire enumeration.  After the RPC call completes, the data is maintained locally.  The <b>HGROUPENUMEX</b> handle contains all of the data required to satisfy the enumeration.  Additional calls to <a href="https://msdn.microsoft.com/139FE5AB-9465-46F8-B360-F27F19D82A88">ClusterGroupEnumEx</a>   or <a href="https://msdn.microsoft.com/28FCEC17-78C6-4902-BC4C-832BE3347380">ClusterGroupGetEnumCountEx</a> do not connect to the cluster.



