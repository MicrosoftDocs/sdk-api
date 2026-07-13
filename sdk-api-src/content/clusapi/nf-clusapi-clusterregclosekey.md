---
UID: NF:clusapi.ClusterRegCloseKey
title: ClusterRegCloseKey function (clusapi.h)
description: Releases the handle of a cluster database key.
helpviewer_keywords: ["ClusterRegCloseKey","ClusterRegCloseKey function [Failover Cluster]","_wolf_clusterregclosekey","clusapi/ClusterRegCloseKey","mscs.clusterregclosekey"]
old-location: mscs\clusterregclosekey.htm
tech.root: MsCS
ms.assetid: 2216ac42-6beb-4ceb-bd15-12bb2886bc6a
ms.date: 12/05/2018
ms.keywords: ClusterRegCloseKey, ClusterRegCloseKey function [Failover Cluster], _wolf_clusterregclosekey, clusapi/ClusterRegCloseKey, mscs.clusterregclosekey
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
 - ClusterRegCloseKey
 - clusapi/ClusterRegCloseKey
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
 - ext-ms-win-cluster-clusapi-l1-1-4.dll
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
api_name:
 - ClusterRegCloseKey
---

# ClusterRegCloseKey function


## -description

Releases the handle of a  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> key.

## -parameters

### -param hKey [in]

Handle to the cluster database key to be closed.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregopenkey">ClusterRegOpenKey</a>