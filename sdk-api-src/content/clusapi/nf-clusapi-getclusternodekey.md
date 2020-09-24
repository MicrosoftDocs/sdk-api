---
UID: NF:clusapi.GetClusterNodeKey
title: GetClusterNodeKey function (clusapi.h)
description: Opens the root of the cluster database subtree for a node.
helpviewer_keywords: ["GetClusterNodeKey","GetClusterNodeKey function [Failover Cluster]","_wolf_getclusternodekey","clusapi/GetClusterNodeKey","mscs.getclusternodekey"]
old-location: mscs\getclusternodekey.htm
tech.root: MsCS
ms.assetid: 8c943e86-aacc-4340-a26a-1d1916150344
ms.date: 12/05/2018
ms.keywords: GetClusterNodeKey, GetClusterNodeKey function [Failover Cluster], _wolf_getclusternodekey, clusapi/GetClusterNodeKey, mscs.getclusternodekey
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
 - GetClusterNodeKey
 - clusapi/GetClusterNodeKey
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
 - GetClusterNodeKey
---

# GetClusterNodeKey function


## -description

Opens the root of the  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> subtree for a  <a href="/previous-versions/windows/desktop/mscs/nodes">node</a>.

## -parameters

### -param hNode [in]

Handle to a node.

### -param samDesired [in]

Access mask that describes the security access needed for the key.

## -returns

If the operation succeeds, the function returns a registry key handle for the node.

If the operation fails, 
the function returns <b>NULL</b>. For more information about the error, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The  <b>GetClusterNodeKey</b> function returns a handle to a cluster database key representing the subtree root for the node identified by <i>hNode</i>. Callers should call  <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregclosekey">ClusterRegCloseKey</a> to close the key handle retrieved by  <b>GetClusterNodeKey</b> when they are done with it.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregclosekey">ClusterRegCloseKey</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternode">OpenClusterNode</a>