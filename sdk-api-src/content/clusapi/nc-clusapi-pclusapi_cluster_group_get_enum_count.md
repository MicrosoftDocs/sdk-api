---
UID: NC:clusapi.PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT
title: PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT
author: windows-driver-content
description: Returns the number of cluster objects associated with a group enumeration handle.
old-location: mscs\clustergroupgetenumcount.htm
old-project: MsCS
ms.assetid: 068cd55e-4220-447c-bf2f-a515503b7cc9
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT, PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT callback function [Failover Cluster], _wolf_clustergroupgetenumcount, clusapi/PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT, mscs.clustergroupgetenumcount
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
req.typenames: LOG_MANAGEMENT_CALLBACKS, *PLOG_MANAGEMENT_CALLBACKS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT callback


## -description


Returns the number of <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">cluster objects</a> associated with a 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a> enumeration handle. The <b>PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT</b> type defines a pointer to this function.


## -parameters




### -param hGroupEnum [in]

Handle to a group enumeration. This handle is obtained from 
      <a href="https://msdn.microsoft.com/d8f9eff0-1784-4b55-8603-c262d5c23f6c">ClusterGroupOpenEnum</a>. A valid handle is 
      required. This parameter cannot be <b>NULL</b>.


## -returns



<i>ClusterGroupGetEnumCount</i> returns the 
       number of objects associated with the enumeration handle.



