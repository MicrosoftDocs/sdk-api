---
UID: NF:clusapi.ResumeClusterNodeEx
title: ResumeClusterNodeEx function (clusapi.h)
description: Initiates the specified failback operation, and then requests that a paused node resumes cluster activity.
old-location: mscs\resumeclusternodeex.htm
tech.root: MsCS
ms.assetid: 6111AA77-8542-4183-98B2-A505889B0B87
ms.date: 12/05/2018
ms.keywords: PCLUSAPI_RESUME_CLUSTER_NODE_EX, PCLUSAPI_RESUME_CLUSTER_NODE_EX function [Failover Cluster], ResumeClusterNodeEx, ResumeClusterNodeEx function [Failover Cluster], clusapi/PCLUSAPI_RESUME_CLUSTER_NODE_EX, clusapi/ResumeClusterNodeEx, mscs.resumeclusternodeex
f1_keywords:
- clusapi/ResumeClusterNodeEx
dev_langs:
- c++
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
- ResumeClusterNodeEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ResumeClusterNodeEx function


## -description


Initiates the specified failback operation, and then requests that a paused node  resumes cluster activity.


## -parameters




### -param hNode [in]

The  handle to the paused node.


### -param eResumeFailbackType [in]

The type of failback operation to use when cluster activity resumes. The available failback types are specified in the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_node_resume_failback_type">CLUSTER_NODE_RESUME_FAILBACK_TYPE</a> enumeration.


### -param dwResumeFlagsReserved [in]

This parameter is reserved for future use.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_node_resume_failback_type">CLUSTER_NODE_RESUME_FAILBACK_TYPE</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/node-management-functions">Node Management Functions</a>
 

 

