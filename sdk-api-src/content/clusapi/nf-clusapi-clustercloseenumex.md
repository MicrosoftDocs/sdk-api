---
UID: NF:clusapi.ClusterCloseEnumEx
title: ClusterCloseEnumEx function (clusapi.h)

description: Closes a handle to an enumeration that was opened by the ClusterOpenEnumEx function.
old-location: mscs\clustercloseenumex.htm
tech.root: MsCS
ms.assetid: B62F1259-C4FF-45FC-9EA1-24CABFE1C0F3

ms.date: 12/05/2018
ms.keywords: ClusterCloseEnumEx, ClusterCloseEnumEx function [Failover Cluster], PCLUSAPI_CLUSTER_CLOSE_ENUM_EX, PCLUSAPI_CLUSTER_CLOSE_ENUM_EX function [Failover Cluster], clusapi/ClusterCloseEnumEx, clusapi/PCLUSAPI_CLUSTER_CLOSE_ENUM_EX, mscs.clustercloseenumex
ms.topic: function
f1_keywords: 
 - "clusapi/ClusterCloseEnumEx"
dev_langs:
 - c++
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 Datacenter, Windows Server 2008 R2 Enterprise
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
 - ClusterCloseEnumEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ClusterCloseEnumEx function


## -description


Closes a handle to an enumeration that was opened by the <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-clusteropenenumex">ClusterOpenEnumEx</a> function.


## -parameters




### -param hClusterEnum [in]

The handle to the cluster enumeration  to close. This is a handle that originally was returned by <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-clusteropenenumex">ClusterOpenEnumEx</a>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-management-functions">Failover Cluster Management Function</a>
 

 

