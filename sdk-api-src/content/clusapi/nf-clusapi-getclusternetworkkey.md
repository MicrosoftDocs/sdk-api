---
UID: NF:clusapi.GetClusterNetworkKey
title: GetClusterNetworkKey function (clusapi.h)
description: Opens the root of the cluster database subtree for a network.
helpviewer_keywords: ["GetClusterNetworkKey","GetClusterNetworkKey function [Failover Cluster]","_wolf_getclusternetworkkey","clusapi/GetClusterNetworkKey","mscs.getclusternetworkkey"]
old-location: mscs\getclusternetworkkey.htm
tech.root: MsCS
ms.assetid: c5d914b4-0419-4c03-bed4-ecb87e44db5e
ms.date: 12/05/2018
ms.keywords: GetClusterNetworkKey, GetClusterNetworkKey function [Failover Cluster], _wolf_getclusternetworkkey, clusapi/GetClusterNetworkKey, mscs.getclusternetworkkey
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetClusterNetworkKey
 - clusapi/GetClusterNetworkKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - GetClusterNetworkKey
---

# GetClusterNetworkKey function


## -description

Opens the root of the  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> subtree for a  <a href="/previous-versions/windows/desktop/mscs/networks">network</a>.

## -parameters

### -param hNetwork [in]

Handle to a network.

### -param samDesired [in]

Access mask that describes the security access needed for the new key.

## -returns

If the operation succeeds, the function returns a registry key handle for the network.

If the operation fails, 
the function returns <b>NULL</b>. For more information about the error, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The  <b>GetClusterNetworkKey</b> function returns a handle to a cluster database key representing the subtree root for the network identified by <i>hNetwork</i>. Callers should call  <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregclosekey">ClusterRegCloseKey</a> to close the key handle retrieved by  <b>GetClusterNetworkKey</b> when they are done with it.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregclosekey">ClusterRegCloseKey</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternetwork">OpenClusterNetwork</a>