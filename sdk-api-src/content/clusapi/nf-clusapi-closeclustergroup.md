---
UID: NF:clusapi.CloseClusterGroup
title: CloseClusterGroup function
author: windows-sdk-content
description: Closes a group handle.
old-location: mscs\closeclustergroup.htm
tech.root: mscs
ms.assetid: 5bbacf45-2e1a-402a-8592-c8f60034c4ad
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: CloseClusterGroup, CloseClusterGroup function [Failover Cluster], PCLUSAPI_CLOSE_CLUSTER_GROUP, PCLUSAPI_CLOSE_CLUSTER_GROUP function [Failover Cluster], _wolf_closeclustergroup, clusapi/CloseClusterGroup, clusapi/PCLUSAPI_CLOSE_CLUSTER_GROUP, mscs.closeclustergroup
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
 - CloseClusterGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CloseClusterGroup function


## -description


Closes a  <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">group</a> handle. The <b>PCLUSAPI_CLOSE_CLUSTER_GROUP</b> type defines a pointer to this function.


## -parameters




### -param hGroup [in]

Handle to the group to close.


## -returns



This function returns BOOL.




## -see-also




<a href="https://msdn.microsoft.com/0c7ef9d9-d32b-448e-9e07-6befb9b3e338">OpenClusterGroup</a>
 

 

