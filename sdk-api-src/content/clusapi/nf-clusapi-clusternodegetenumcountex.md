---
UID: NF:clusapi.ClusterNodeGetEnumCountEx
title: ClusterNodeGetEnumCountEx function (clusapi.h)
author: windows-sdk-content
description: Returns the number of cluster objects that are associated with a node enumeration handle.
old-location: mscs\clusternodegetenumcountex.htm
tech.root: MsCS
ms.assetid: 5C45ED88-9CB4-4C20-97D1-6F02A51048CE
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ClusterNodeGetEnumCountEx, ClusterNodeGetEnumCountEx function [Failover Cluster], PCLUSAPI_CLUSTER_NODE_GET_ENUM_COUNT_EX, PCLUSAPI_CLUSTER_NODE_GET_ENUM_COUNT_EX function [Failover Cluster], clusapi/ClusterNodeGetEnumCountEx, clusapi/PCLUSAPI_CLUSTER_NODE_GET_ENUM_COUNT_EX, mscs.clusternodegetenumcountex
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 Datacenter, Windows Server 2008 R2 Enterprise
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
 - ClusterNodeGetEnumCountEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterNodeGetEnumCountEx function


## -description


Returns the number of 
cluster objects that are associated with a 
node enumeration handle.


## -parameters




### -param hNodeEnum [in]

The handle to a node enumeration that was retrieved by the   <a href="https://msdn.microsoft.com/A251C5A3-2C9F-4030-8013-4846AD83A2E9">ClusterNodeOpenEnumEx</a> function. A valid handle is required. This parameter cannot be <b>NULL</b>.


## -returns



The number of objects that are associated with the enumeration handle.




## -see-also




<a href="https://msdn.microsoft.com/18981eec-42c0-4e31-8e5c-b79d8ff89fc8">Node Management Functions</a>
 

 

