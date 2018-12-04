---
UID: NF:clusapi.ClusterResourceCloseEnum
title: ClusterResourceCloseEnum function
author: windows-sdk-content
description: Closes a resource enumeration handle.
old-location: mscs\clusterresourcecloseenum.htm
tech.root: mscs
ms.assetid: 49407b45-2b7f-43a2-90ff-98cc557edb31
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ClusterResourceCloseEnum, ClusterResourceCloseEnum function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM, PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM function [Failover Cluster], _wolf_clusterresourcecloseenum, clusapi/ClusterResourceCloseEnum, clusapi/PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM, mscs.clusterresourcecloseenum
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
 - Ext-MS-Win-Cluster-ClusAPI-L1-1-2.dll
api_name:
 - ClusterResourceCloseEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterResourceCloseEnum function


## -description


Closes a  <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> enumeration handle. The <b>PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM</b> type defines a pointer to this function.


## -parameters




### -param hResEnum [in]

A resource enumeration handle to be closed.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.
     If the operation fails, 
the function returns a different <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/d1f7360d-f592-49fb-b3b4-60d93afd7c6f">Cluster Resource Management Functions</a>



<a href="https://msdn.microsoft.com/73627594-90df-496d-8120-b24c34f13fb5">ClusterResourceEnum</a>



<a href="https://msdn.microsoft.com/f801401f-f49d-41de-b88b-b832330eeccf">ClusterResourceOpenEnum</a>
 

 

