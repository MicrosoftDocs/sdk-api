---
UID: NF:clusapi.GetClusterResourceTypeKey
title: GetClusterResourceTypeKey function (clusapi.h)
description: Opens the root of the cluster database subtree for a resource type.
helpviewer_keywords: ["GetClusterResourceTypeKey","GetClusterResourceTypeKey function [Failover Cluster]","_wolf_getclusterresourcetypekey","clusapi/GetClusterResourceTypeKey","mscs.getclusterresourcetypekey"]
old-location: mscs\getclusterresourcetypekey.htm
tech.root: MsCS
ms.assetid: facc22b2-221d-4d82-85ae-5b9a463c5858
ms.date: 12/05/2018
ms.keywords: GetClusterResourceTypeKey, GetClusterResourceTypeKey function [Failover Cluster], _wolf_getclusterresourcetypekey, clusapi/GetClusterResourceTypeKey, mscs.getclusterresourcetypekey
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
 - GetClusterResourceTypeKey
 - clusapi/GetClusterResourceTypeKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-clusapi-l1-1-6.dll
 - ext-ms-win-cluster-clusapi-l1-1-5.dll
 - ClusAPI.dll
api_name:
 - GetClusterResourceTypeKey
---

# GetClusterResourceTypeKey function


## -description

Opens the root of the  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> subtree for a  <a href="/previous-versions/windows/desktop/mscs/resource-types">resource type</a>.

## -parameters

### -param hCluster [in]

Handle to a <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a>.

### -param lpszTypeName [in]

Pointer to a NULL-terminated Unicode string specifying the name of a resource type (the registered type name, not the display name).

### -param samDesired [in]

Access mask that describes the security access needed for the opened key.

## -returns

If the operation succeeds, the function returns a registry key handle for the resource type.

If the operation fails, 
the function returns <b>NULL</b>. For more information about the error, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The  <b>GetClusterResourceTypeKey</b> function returns a handle to a cluster database key representing the subtree root for the resource type pointed to by <i>lpszTypeName</i> in the cluster identified by <i>hCluster</i>. Callers should call  <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregclosekey">ClusterRegCloseKey</a> to close the key handle retrieved by  <b>GetClusterResourceTypeKey</b> when they are done with it.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregclosekey">ClusterRegCloseKey</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>