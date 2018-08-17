---
UID: NF:clusapi.ClusterNodeGetEnumCount
title: ClusterNodeGetEnumCount function
author: windows-sdk-content
description: Returns the number of cluster objects associated with a node enumeration handle.
old-location: mscs\clusternodegetenumcount.htm
old-project: mscs
ms.assetid: bec31b84-a4fd-48a3-b465-ceebb1f61028
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusterNodeGetEnumCount, ClusterNodeGetEnumCount function [Failover Cluster], PCLUSAPI_CLUSTER_NODE_GET_ENUM_COUNT, PCLUSAPI_CLUSTER_NODE_GET_ENUM_COUNT function [Failover Cluster], _wolf_clusternodegetenumcount, clusapi/ClusterNodeGetEnumCount, clusapi/PCLUSAPI_CLUSTER_NODE_GET_ENUM_COUNT, mscs.clusternodegetenumcount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.redist: 
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
 - ClusterNodeGetEnumCount
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# ClusterNodeGetEnumCount function


## -description


Returns the number of  <a href="https://msdn.microsoft.com/en-us/library/Aa369115(v=VS.85).aspx">cluster objects</a> associated with a  <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a> enumeration handle.


## -parameters




### -param hNodeEnum [in]

Handle to a node enumeration. This handle is obtained from  <a href="https://msdn.microsoft.com/f187f4d7-24c8-477d-91fc-0ef738b66f22">ClusterNodeOpenEnum</a>. A valid handle is required. This parameter cannot be <b>NULL</b>.


## -returns



<b>ClusterNodeGetEnumCount</b> returns the number of objects associated with the enumeration handle.



