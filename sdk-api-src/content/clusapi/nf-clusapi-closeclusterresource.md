---
UID: NF:clusapi.CloseClusterResource
title: CloseClusterResource function
author: windows-sdk-content
description: Closes a resource handle.
old-location: mscs\closeclusterresource.htm
tech.root: MsCS
ms.assetid: dbefd7f9-3499-45b3-a5c8-d0000632f61c
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: CloseClusterResource, CloseClusterResource function [Failover Cluster], PCLUSAPI_CLOSE_CLUSTER_RESOURCE, PCLUSAPI_CLOSE_CLUSTER_RESOURCE function [Failover Cluster], _wolf_closeclusterresource, clusapi/CloseClusterResource, clusapi/PCLUSAPI_CLOSE_CLUSTER_RESOURCE, mscs.closeclusterresource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clusapi.h
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
 - CloseClusterResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CloseClusterResource function


## -description


Closes a  <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource</a> handle. The <b>PCLUSAPI_CLOSE_CLUSTER_RESOURCE</b> type defines a pointer to this function.


## -parameters




### -param hResource [in]

Handle to the resource to be closed.


## -returns



This function returns BOOL.




## -see-also




<a href="https://msdn.microsoft.com/c9fe8fa8-57d7-4866-8113-694dc44dae22">CreateClusterResource</a>



<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>
 

 

