---
UID: NF:clusapi.GetClusterResourceKey
title: GetClusterResourceKey function (clusapi.h)
description: Opens the root of the cluster database subtree for a resource.
old-location: mscs\getclusterresourcekey.htm
tech.root: MsCS
ms.assetid: 841f28a1-1415-41bb-b8ac-cf17c6d7c6f3
ms.date: 12/05/2018
ms.keywords: GetClusterResourceKey, GetClusterResourceKey function [Failover Cluster], _wolf_getclusterresourcekey, clusapi/GetClusterResourceKey, mscs.getclusterresourcekey
ms.topic: function
f1_keywords:
- clusapi/GetClusterResourceKey
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
- GetClusterResourceKey
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetClusterResourceKey function


## -description


Opens the root of the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> subtree for a  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resources">resource</a>.


## -parameters




### -param hResource [in]

Handle to a resource.


### -param samDesired [in]

Access mask that describes the security access needed for the opened key.


## -returns



If the operation succeeds, the function returns a registry key handle for the resource.

If the operation fails, 
the function returns <b>NULL</b>. For more information about the error, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The  <b>GetClusterResourceKey</b> function returns a handle to a cluster database key representing the subtree root for the resource identified by <i>hResource</i>. Callers should call  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregclosekey">ClusterRegCloseKey</a> to close the key handle retrieved by  <b>GetClusterResourceKey</b> when they are done with it.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregclosekey">ClusterRegCloseKey</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-openclusterresource">OpenClusterResource</a>
 

 

