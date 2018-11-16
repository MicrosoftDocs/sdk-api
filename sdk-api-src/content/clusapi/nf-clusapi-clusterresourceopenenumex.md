---
UID: NF:clusapi.ClusterResourceOpenEnumEx
title: ClusterResourceOpenEnumEx function
author: windows-sdk-content
description: Opens a handle to a resource enumeration that enables iteration through a resource's dependencies and nodes.
old-location: mscs\clusterresourceopenenumex.htm
tech.root: MsCS
ms.assetid: B43460F1-4BFE-48E0-889A-56370320E4E6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ClusterResourceOpenEnumEx, ClusterResourceOpenEnumEx function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_OPEN_ENUM_EX, PCLUSAPI_CLUSTER_RESOURCE_OPEN_ENUM_EX function [Failover Cluster], clusapi/ClusterResourceOpenEnumEx, clusapi/PCLUSAPI_CLUSTER_RESOURCE_OPEN_ENUM_EX, mscs.clusterresourceopenenumex
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
 - ClusterResourceOpenEnumEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ClusterResourceOpenEnumEx
: 
---

# ClusterResourceOpenEnumEx function


## -description


Opens a handle to a  resource enumeration  that  enables iteration   through a resource's dependencies and nodes.




## -parameters




### -param hCluster [in]

A handle to the resource to iterate through.


### -param lpszProperties [in, optional]

A pointer to a list of names of common properties.


### -param cbProperties [in]

The size, in bytes, of the <i>lpszProperties</i>  parameter.


### -param lpszRoProperties [in, optional]

A pointer to a list of names of read-only common properties.


### -param cbRoProperties [in]

The size, in bytes, of the <i>lpszRoProperties</i>  parameter.


### -param dwFlags [in]

The index that identifies the next object to enumerate. This parameter should be zero for the first call to <b>ClusterResourceOpenEnumEx</b> and then be incremented for subsequent calls.


## -returns



If the operation succeeds, the function returns an enumeration handle.

If the operation fails, the function returns <b>NULL</b>. For more information about the 
       error, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d1f7360d-f592-49fb-b3b4-60d93afd7c6f">Failover Cluster Resource Management Functions</a>
 

 

