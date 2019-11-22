---
UID: NF:clusapi.ClusterNodeCloseEnum
title: ClusterNodeCloseEnum function (clusapi.h)

description: Closes a node enumeration handle.
old-location: mscs\clusternodecloseenum.htm
tech.root: MsCS
ms.assetid: 8133125f-eb5a-4cbc-a39d-72fb5f3ee384

ms.date: 12/05/2018
ms.keywords: ClusterNodeCloseEnum, ClusterNodeCloseEnum function [Failover Cluster], PCLUSAPI_CLUSTER_NODE_CLOSE_ENUM, PCLUSAPI_CLUSTER_NODE_CLOSE_ENUM function [Failover Cluster], _wolf_clusternodecloseenum, clusapi/ClusterNodeCloseEnum, clusapi/PCLUSAPI_CLUSTER_NODE_CLOSE_ENUM, mscs.clusternodecloseenum
ms.topic: function
f1_keywords: 
 - "clusapi/ClusterNodeCloseEnum"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ClusterNodeCloseEnum function


## -description


Closes a  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/nodes">node</a> enumeration handle. The <b>PCLUSAPI_CLUSTER_NODE_CLOSE_ENUM</b> type defines a pointer to this function.


## -parameters




### -param hNodeEnum [in]

Handle to the node enumerator to close. This is a handle originally returned by the  <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-clusternodeopenenum">ClusterNodeOpenEnum</a> function.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.
     If the operation fails, 
the function returns a <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-clusternodeenum">ClusterNodeEnum</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-clusternodeopenenum">ClusterNodeOpenEnum</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/node-management-functions">Node Management Functions</a>
 

 

