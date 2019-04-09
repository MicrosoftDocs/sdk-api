---
UID: NF:clusapi.ClusterCloseEnum
title: ClusterCloseEnum function (clusapi.h)
author: windows-sdk-content
description: Closes a cluster enumeration handle originally opened by ClusterOpenEnum.
old-location: mscs\clustercloseenum.htm
tech.root: MsCS
ms.assetid: 3d7e45a0-d580-4d14-8795-2418bba40c73
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ClusterCloseEnum, ClusterCloseEnum function [Failover Cluster], PCLUSAPI_CLUSTER_CLOSE_ENUM, PCLUSAPI_CLUSTER_CLOSE_ENUM function [Failover Cluster], _wolf_clustercloseenum, clusapi/ClusterCloseEnum, clusapi/PCLUSAPI_CLUSTER_CLOSE_ENUM, mscs.clustercloseenum
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
 - ClusterCloseEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterCloseEnum function


## -description


Closes a cluster enumeration handle originally opened by  <a href="https://msdn.microsoft.com/b6eb5c03-dd6e-42ef-a020-cf0d61143040">ClusterOpenEnum</a>.


## -parameters




### -param hEnum [in]

Cluster enumeration handle to close. This is a handle originally returned by the  <a href="https://msdn.microsoft.com/b6eb5c03-dd6e-42ef-a020-cf0d61143040">ClusterOpenEnum</a> function.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/a7511ac6-04cb-407b-90aa-3382c5160cb6">ClusterEnum</a>



<a href="https://msdn.microsoft.com/b6eb5c03-dd6e-42ef-a020-cf0d61143040">ClusterOpenEnum</a>
 

 

