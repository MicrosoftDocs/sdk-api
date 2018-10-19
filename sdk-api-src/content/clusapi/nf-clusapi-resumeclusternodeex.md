---
UID: NF:clusapi.ResumeClusterNodeEx
title: ResumeClusterNodeEx function
author: windows-sdk-content
description: Initiates the specified failback operation, and then requests that a paused node resumes cluster activity.
old-location: mscs\resumeclusternodeex.htm
tech.root: mscs
ms.assetid: 6111AA77-8542-4183-98B2-A505889B0B87
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: PCLUSAPI_RESUME_CLUSTER_NODE_EX, PCLUSAPI_RESUME_CLUSTER_NODE_EX function [Failover Cluster], ResumeClusterNodeEx, ResumeClusterNodeEx function [Failover Cluster], clusapi/PCLUSAPI_RESUME_CLUSTER_NODE_EX, clusapi/ResumeClusterNodeEx, mscs.resumeclusternodeex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResumeClusterNodeEx function


## -description


Initiates the specified failback operation, and then requests that a paused node  resumes cluster activity.


## -parameters




### -param hNode [in]

The  handle to the paused node.


### -param eResumeFailbackType [in]

The type of failback operation to use when cluster activity resumes. The available failback types are specified in the <a href="https://msdn.microsoft.com/en-us/library/Dn622913(v=VS.85).aspx">CLUSTER_NODE_RESUME_FAILBACK_TYPE</a> enumeration.


### -param dwResumeFlagsReserved [in]

This parameter is reserved for future use.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn622913(v=VS.85).aspx">CLUSTER_NODE_RESUME_FAILBACK_TYPE</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa371760(v=VS.85).aspx">Node Management Functions</a>
 

 

