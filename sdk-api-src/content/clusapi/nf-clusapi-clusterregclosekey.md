---
UID: NF:clusapi.ClusterRegCloseKey
title: ClusterRegCloseKey function (clusapi.h)
author: windows-sdk-content
description: Releases the handle of a cluster database key.
old-location: mscs\clusterregclosekey.htm
tech.root: MsCS
ms.assetid: 2216ac42-6beb-4ceb-bd15-12bb2886bc6a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ClusterRegCloseKey, ClusterRegCloseKey function [Failover Cluster], _wolf_clusterregclosekey, clusapi/ClusterRegCloseKey, mscs.clusterregclosekey
ms.topic: function
f1_keywords: 
 - "clusapi/ClusterRegCloseKey"
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
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
api_name:
 - ClusterRegCloseKey
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ClusterRegCloseKey function


## -description


Releases the handle of a  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> key.


## -parameters




### -param hKey [in]

Handle to the cluster database key to be closed.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregopenkey">ClusterRegOpenKey</a>
 

 

