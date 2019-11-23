---
UID: NF:clusapi.GetClusterKey
title: GetClusterKey function (clusapi.h)

description: Opens the root of the cluster database subtree for a cluster.
old-location: mscs\getclusterkey.htm
tech.root: MsCS
ms.assetid: ddec12fc-6d4d-411d-ab24-6fb60175ba7b

ms.date: 12/05/2018
ms.keywords: GetClusterKey, GetClusterKey function [Failover Cluster], _wolf_getclusterkey, clusapi/GetClusterKey, mscs.getclusterkey
ms.topic: function
f1_keywords: 
 - "clusapi/GetClusterKey"
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
 - GetClusterKey
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetClusterKey function


## -description


Opens the root of the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> subtree for a 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/c-gly">cluster</a>.


## -parameters




### -param hCluster [in]

Handle to a cluster.


### -param samDesired [in]

Access mask that describes the security access needed for the new key. For more information and possible 
      values, see 
      <a href="https://docs.microsoft.com/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.


## -returns



If the operation succeeds, the function returns a database key handle for the cluster.

If the operation fails, the function returns <b>NULL</b>. For more information about the error, call 
       <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The <b>GetClusterKey</b> function returns a handle to a 
    cluster database key representing the cluster database subtree root for the cluster identified by 
    <i>hCluster</i>. Callers should call 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregclosekey">ClusterRegCloseKey</a> to close the key handle 
    retrieved by <b>GetClusterKey</b> when they are done with it.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregclosekey">ClusterRegCloseKey</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>
 

 

