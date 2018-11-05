---
UID: NF:clusapi.ClusterNodeCloseEnum
title: ClusterNodeCloseEnum function
author: windows-sdk-content
description: Closes a node enumeration handle.
old-location: mscs\clusternodecloseenum.htm
tech.root: mscs
ms.assetid: 8133125f-eb5a-4cbc-a39d-72fb5f3ee384
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ClusterNodeCloseEnum, ClusterNodeCloseEnum function [Failover Cluster], PCLUSAPI_CLUSTER_NODE_CLOSE_ENUM, PCLUSAPI_CLUSTER_NODE_CLOSE_ENUM function [Failover Cluster], _wolf_clusternodecloseenum, clusapi/ClusterNodeCloseEnum, clusapi/PCLUSAPI_CLUSTER_NODE_CLOSE_ENUM, mscs.clusternodecloseenum
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
api_name:
 - ClusterNodeCloseEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterNodeCloseEnum function


## -description


Closes a  <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a> enumeration handle. The <b>PCLUSAPI_CLUSTER_NODE_CLOSE_ENUM</b> type defines a pointer to this function.


## -parameters




### -param hNodeEnum [in]

Handle to the node enumerator to close. This is a handle originally returned by the  <a href="https://msdn.microsoft.com/f187f4d7-24c8-477d-91fc-0ef738b66f22">ClusterNodeOpenEnum</a> function.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.
     If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/e184ef8e-9ec6-4d84-a3d0-850298262b81">ClusterNodeEnum</a>



<a href="https://msdn.microsoft.com/f187f4d7-24c8-477d-91fc-0ef738b66f22">ClusterNodeOpenEnum</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa371760(v=VS.85).aspx">Node Management Functions</a>
 

 

