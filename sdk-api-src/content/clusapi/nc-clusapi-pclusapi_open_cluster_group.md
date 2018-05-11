---
UID: NC:clusapi.PCLUSAPI_OPEN_CLUSTER_GROUP
title: PCLUSAPI_OPEN_CLUSTER_GROUP
author: windows-driver-content
description: Opens a failover cluster group and returns a handle to it.
old-location: mscs\openclustergroup.htm
old-project: MsCS
ms.assetid: 0c7ef9d9-d32b-448e-9e07-6befb9b3e338
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: PCLUSAPI_OPEN_CLUSTER_GROUP, PCLUSAPI_OPEN_CLUSTER_GROUP callback, PCLUSAPI_OPEN_CLUSTER_GROUP callback function [Failover Cluster], _wolf_openclustergroup, clusapi/PCLUSAPI_OPEN_CLUSTER_GROUP, mscs.openclustergroup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_OPEN_CLUSTER_GROUP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_OPEN_CLUSTER_GROUP callback function


## -description


Opens a failover cluster <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a> and returns a handle to 
    it.


## -parameters




### -param hCluster [in]

Handle to a cluster that includes the group to open.


### -param lpszGroupName [in]

Name of the group to open.


## -returns



If the operation was successful, 
       <i>OpenClusterGroup</i> returns a group handle.




## -see-also




<a href="https://msdn.microsoft.com/5bbacf45-2e1a-402a-8592-c8f60034c4ad">CloseClusterGroup</a>



<a href="https://msdn.microsoft.com/a2336594-ac24-476e-94e8-460a31c1f643">Group Management Functions</a>



<a href="https://msdn.microsoft.com/240defbb-b9e9-4455-b863-c9b2192f12b7">OpenClusterGroupEx</a>
 

 

