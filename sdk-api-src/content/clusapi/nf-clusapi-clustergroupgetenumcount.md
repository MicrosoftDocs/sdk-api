---
UID: NF:clusapi.ClusterGroupGetEnumCount
title: ClusterGroupGetEnumCount function
author: windows-sdk-content
description: Returns the number of cluster objects associated with a group enumeration handle.
old-location: mscs\clustergroupgetenumcount.htm
tech.root: mscs
ms.assetid: 068cd55e-4220-447c-bf2f-a515503b7cc9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ClusterGroupGetEnumCount, ClusterGroupGetEnumCount function [Failover Cluster], PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT, PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT function [Failover Cluster], _wolf_clustergroupgetenumcount, clusapi/ClusterGroupGetEnumCount, clusapi/PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT, mscs.clustergroupgetenumcount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
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
 - ClusterGroupGetEnumCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterGroupGetEnumCount function


## -description


Returns the number of <a href="https://msdn.microsoft.com/en-us/library/Aa369115(v=VS.85).aspx">cluster objects</a> associated with a 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369645(v=VS.85).aspx">group</a> enumeration handle. The <b>PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT</b> type defines a pointer to this function.


## -parameters




### -param hGroupEnum [in]

Handle to a group enumeration. This handle is obtained from 
      <a href="https://msdn.microsoft.com/d8f9eff0-1784-4b55-8603-c262d5c23f6c">ClusterGroupOpenEnum</a>. A valid handle is 
      required. This parameter cannot be <b>NULL</b>.


## -returns



<b>ClusterGroupGetEnumCount</b> returns the 
       number of objects associated with the enumeration handle.



