---
UID: NC:clusapi.PCLUSAPI_CLUSTER_NODE_GET_ENUM_COUNT
title: PCLUSAPI_CLUSTER_NODE_GET_ENUM_COUNT
author: windows-driver-content
description: Returns the number of cluster objects associated with a node enumeration handle.
old-location: mscs\clusternodegetenumcount.htm
old-project: MsCS
ms.assetid: bec31b84-a4fd-48a3-b465-ceebb1f61028
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PCLUSAPI_CLUSTER_NODE_GET_ENUM_COUNT, PCLUSAPI_CLUSTER_NODE_GET_ENUM_COUNT callback function [Failover Cluster], _wolf_clusternodegetenumcount, clusapi/PCLUSAPI_CLUSTER_NODE_GET_ENUM_COUNT, mscs.clusternodegetenumcount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_CLUSTER_NODE_GET_ENUM_COUNT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLUSTER_NODE_GET_ENUM_COUNT callback


## -description


Returns the number of  <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">cluster objects</a> associated with a  <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> enumeration handle.


## -parameters




### -param hNodeEnum [in]

Handle to a node enumeration. This handle is obtained from  <a href="https://msdn.microsoft.com/f187f4d7-24c8-477d-91fc-0ef738b66f22">ClusterNodeOpenEnum</a>. A valid handle is required. This parameter cannot be <b>NULL</b>.


## -returns



<i>ClusterNodeGetEnumCount</i> returns the number of objects associated with the enumeration handle.



