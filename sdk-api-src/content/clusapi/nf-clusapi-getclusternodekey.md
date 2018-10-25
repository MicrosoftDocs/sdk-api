---
UID: NF:clusapi.GetClusterNodeKey
title: GetClusterNodeKey function
author: windows-sdk-content
description: Opens the root of the cluster database subtree for a node.
old-location: mscs\getclusternodekey.htm
tech.root: mscs
ms.assetid: 8c943e86-aacc-4340-a26a-1d1916150344
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: GetClusterNodeKey, GetClusterNodeKey function [Failover Cluster], _wolf_getclusternodekey, clusapi/GetClusterNodeKey, mscs.getclusternodekey
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
 - GetClusterNodeKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetClusterNodeKey function


## -description


Opens the root of the  <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> subtree for a  <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a>.


## -parameters




### -param hNode [in]

Handle to a node.


### -param samDesired [in]

Access mask that describes the security access needed for the key.


## -returns



If the operation succeeds, the function returns a registry key handle for the node.

If the operation fails, 
the function returns <b>NULL</b>. For more information about the error, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The  <b>GetClusterNodeKey</b> function returns a handle to a cluster database key representing the subtree root for the node identified by <i>hNode</i>. Callers should call  <a href="https://msdn.microsoft.com/2216ac42-6beb-4ceb-bd15-12bb2886bc6a">ClusterRegCloseKey</a> to close the key handle retrieved by  <b>GetClusterNodeKey</b> when they are done with it.




## -see-also




<a href="https://msdn.microsoft.com/2216ac42-6beb-4ceb-bd15-12bb2886bc6a">ClusterRegCloseKey</a>



<a href="https://msdn.microsoft.com/7658a030-d4b2-407c-829f-61491b5907e6">OpenClusterNode</a>
 

 

