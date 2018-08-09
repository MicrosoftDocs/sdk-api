---
UID: NF:clusapi.CloseClusterGroupSet
title: CloseClusterGroupSet function
author: windows-sdk-content
description: Closes a groupset handle returned from OpenClusterGroupSet.
old-location: mscs\closeclustergroupcollection.htm
old-project: mscs
ms.assetid: 017f0c40-023d-4b22-90ec-037122718830
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CloseClusterGroupSet, CloseClusterGroupSet function [Failover Cluster], PCLUSAPI_CLOSE_CLUSTER_GROUP_SET, PCLUSAPI_CLOSE_CLUSTER_GROUP_SET function [Failover Cluster], clusapi/CloseClusterGroupSet, clusapi/PCLUSAPI_CLOSE_CLUSTER_GROUP_SET, mscs.closeclustergroupcollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
api_name:
 - CloseClusterGroupSet
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# CloseClusterGroupSet function


## -description


Closes a groupset handle returned from <a href="https://msdn.microsoft.com/8a5b944b-53c2-4437-b580-6ad603d0011a">OpenClusterGroupSet</a>.


## -parameters




### -param hGroupSet [in]

The handle to close


## -returns



This function returns BOOL.



