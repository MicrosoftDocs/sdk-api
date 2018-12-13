---
UID: NF:clusapi.GetClusterKey
title: GetClusterKey function
author: windows-sdk-content
description: Opens the root of the cluster database subtree for a cluster.
old-location: mscs\getclusterkey.htm
tech.root: mscs
ms.assetid: ddec12fc-6d4d-411d-ab24-6fb60175ba7b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetClusterKey, GetClusterKey function [Failover Cluster], _wolf_getclusterkey, clusapi/GetClusterKey, mscs.getclusterkey
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
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - GetClusterKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetClusterKey function


## -description


Opens the root of the 
    <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> subtree for a 
    <a href="c_gly.htm">cluster</a>.


## -parameters




### -param hCluster [in]

Handle to a cluster.


### -param samDesired [in]

Access mask that describes the security access needed for the new key. For more information and possible 
      values, see 
      <a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>.


## -returns



If the operation succeeds, the function returns a database key handle for the cluster.

If the operation fails, the function returns <b>NULL</b>. For more information about the error, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>GetClusterKey</b> function returns a handle to a 
    cluster database key representing the cluster database subtree root for the cluster identified by 
    <i>hCluster</i>. Callers should call 
    <a href="https://msdn.microsoft.com/2216ac42-6beb-4ceb-bd15-12bb2886bc6a">ClusterRegCloseKey</a> to close the key handle 
    retrieved by <b>GetClusterKey</b> when they are done with it.




## -see-also




<a href="https://msdn.microsoft.com/2216ac42-6beb-4ceb-bd15-12bb2886bc6a">ClusterRegCloseKey</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>
 

 

