---
UID: NF:clusapi.OpenClusterGroup
title: OpenClusterGroup function
author: windows-sdk-content
description: Opens a failover cluster group and returns a handle to it.
old-location: mscs\openclustergroup.htm
old-project: mscs
ms.assetid: 0c7ef9d9-d32b-448e-9e07-6befb9b3e338
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: OpenClusterGroup, OpenClusterGroup function [Failover Cluster], PCLUSAPI_OPEN_CLUSTER_GROUP, PCLUSAPI_OPEN_CLUSTER_GROUP function [Failover Cluster], _wolf_openclustergroup, clusapi/OpenClusterGroup, clusapi/PCLUSAPI_OPEN_CLUSTER_GROUP, mscs.openclustergroup
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SR_REPLICATED_DISK_TYPE, *PSR_REPLICATED_DISK_TYPE
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
 - OpenClusterGroup
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# OpenClusterGroup function


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
       <b>OpenClusterGroup</b> returns a group handle.




## -see-also




<a href="https://msdn.microsoft.com/5bbacf45-2e1a-402a-8592-c8f60034c4ad">CloseClusterGroup</a>



<a href="https://msdn.microsoft.com/a2336594-ac24-476e-94e8-460a31c1f643">Group Management Functions</a>



<a href="https://msdn.microsoft.com/240defbb-b9e9-4455-b863-c9b2192f12b7">OpenClusterGroupEx</a>
 

 

