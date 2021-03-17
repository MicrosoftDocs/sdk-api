---
UID: NF:clusapi.GetClusterGroupKey
title: GetClusterGroupKey function (clusapi.h)
description: Opens the root of the cluster database subtree for a group.
helpviewer_keywords: ["GetClusterGroupKey","GetClusterGroupKey function [Failover Cluster]","_wolf_getclustergroupkey","clusapi/GetClusterGroupKey","mscs.getclustergroupkey"]
old-location: mscs\getclustergroupkey.htm
tech.root: MsCS
ms.assetid: 86f34e31-f240-485f-a5b6-e4de922b8d97
ms.date: 12/05/2018
ms.keywords: GetClusterGroupKey, GetClusterGroupKey function [Failover Cluster], _wolf_getclustergroupkey, clusapi/GetClusterGroupKey, mscs.getclustergroupkey
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
 - GetClusterGroupKey
 - clusapi/GetClusterGroupKey
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
 - GetClusterGroupKey
---

# GetClusterGroupKey function


## -description

Opens the root of the  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> subtree for a  <a href="/previous-versions/windows/desktop/mscs/groups">group</a>.

## -parameters

### -param hGroup [in]

Handle to a group.

### -param samDesired [in]

Access mask that describes the security access needed for the key.

## -returns

If the operation succeeds, the function returns a database key handle for the group.

If the operation fails, 
the function returns <b>NULL</b>. For more information about the error, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The  <b>GetClusterGroupKey</b> function returns a handle to a cluster database key representing the subtree root for the group identified by <i>hGroup</i>. Callers should call  <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregclosekey">ClusterRegCloseKey</a> to close the key handle retrieved by  <b>GetClusterGroupKey</b> when they are done with it.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregclosekey">ClusterRegCloseKey</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclustergroup">OpenClusterGroup</a>