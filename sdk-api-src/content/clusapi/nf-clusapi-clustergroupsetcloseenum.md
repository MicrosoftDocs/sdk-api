---
UID: NF:clusapi.ClusterGroupSetCloseEnum
title: ClusterGroupSetCloseEnum function
author: windows-sdk-content
description: Closes an open enumeration for a groupset.
old-location: mscs\clustergroupcollectioncloseenum.htm
old-project: mscs
ms.assetid: b82e13f0-364c-41cf-9fda-98a95f23ff7d
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: ClusterGroupSetCloseEnum, ClusterGroupSetCloseEnum function [Failover Cluster], PCLUSAPI_CLOSE_CLUSTER_GROUP_GROUPSET, PCLUSAPI_CLOSE_CLUSTER_GROUP_GROUPSET function [Failover Cluster], clusapi/ClusterGroupSetCloseEnum, clusapi/PCLUSAPI_CLOSE_CLUSTER_GROUP_GROUPSET, mscs.clustergroupcollectioncloseenum
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
 - ClusterGroupSetCloseEnum
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# ClusterGroupSetCloseEnum function


## -description


Closes an open enumeration for a groupset.


## -parameters




### -param hGroupSetEnum

TBD




#### - hGroupCollectionEnum [in]

The enumeration to be closed.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.



