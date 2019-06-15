---
UID: NF:clusapi.ClusterNodeOpenEnumEx
title: ClusterNodeOpenEnumEx function (clusapi.h)
author: windows-sdk-content
description: Opens an enumerator that can iterate through the network interfaces or groups that are installed on a node.
old-location: mscs\clusternodeopenenumex.htm
tech.root: MsCS
ms.assetid: A251C5A3-2C9F-4030-8013-4846AD83A2E9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ClusterNodeOpenEnumEx, ClusterNodeOpenEnumEx function [Failover Cluster], PCLUSAPI_CLUSTER_NODE_OPEN_ENUM_EX, PCLUSAPI_CLUSTER_NODE_OPEN_ENUM_EX function [Failover Cluster], clusapi/ClusterNodeOpenEnumEx, clusapi/PCLUSAPI_CLUSTER_NODE_OPEN_ENUM_EX, mscs.clusternodeopenenumex
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
 - kbSyntax
api_type:
 - <TBD>
api_location:
 -
api_name:
 - ClusterNodeOpenEnumEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ClusterNodeOpenEnumEx function


## -description


Opens an 
    enumerator that can iterate through the network interfaces  
    or groups that are installed on a node.


## -parameters




### -param hNode [in]

A handle to the  node.


### -param dwType [in]

A bitmask that describes the type of objects to enumerate. This parameter  is retrieved from a 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_node_enum">CLUSTER_NODE_ENUM</a> enumeration value.


### -param pOptions [in, optional] [in, optional]

TBD


## -returns



If the operation succeeds, 
       the <b>ClusterNodeOpenEnumEx</b>  function  returns a handle to a node 
       enumerator.

If the operation fails, the function returns <b>NULL</b>. For more information about the 
       error, call the <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/node-management-functions">Node Management Functions</a>
 

 

