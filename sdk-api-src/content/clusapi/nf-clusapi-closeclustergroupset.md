---
UID: NF:clusapi.CloseClusterGroupSet
title: CloseClusterGroupSet function
author: windows-sdk-content
description: Closes a groupset handle returned from OpenClusterGroupSet.
old-location: mscs\closeclustergroupcollection.htm
tech.root: mscs
ms.assetid: 017f0c40-023d-4b22-90ec-037122718830
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: CloseClusterGroupSet, CloseClusterGroupSet function [Failover Cluster], PCLUSAPI_CLOSE_CLUSTER_GROUP_SET, PCLUSAPI_CLOSE_CLUSTER_GROUP_SET function [Failover Cluster], clusapi/CloseClusterGroupSet, clusapi/PCLUSAPI_CLOSE_CLUSTER_GROUP_SET, mscs.closeclustergroupcollection
ms.prod: windows-hardware
ms.technology: windows-devices
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
api_name:
 - CloseClusterGroupSet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CloseClusterGroupSet function


## -description


Closes a groupset handle returned from <a href="https://msdn.microsoft.com/8a5b944b-53c2-4437-b580-6ad603d0011a">OpenClusterGroupSet</a>.


## -parameters




### -param hGroupSet [in]

The handle to close


## -returns



This function returns BOOL.



