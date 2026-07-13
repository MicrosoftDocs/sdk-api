---
UID: NF:clusapi.ClusterSetAccountAccess
title: ClusterSetAccountAccess function (clusapi.h)
description: Updates an account access list (ACL) for a cluster.
helpviewer_keywords: ["CLUSAPI_ALL_ACCESS","CLUSAPI_CHANGE_ACCESS","CLUSAPI_NO_ACCESS","CLUSAPI_READ_ACCESS","CLUSTER_DELETE_ACCESS_CONTROL_ENTRY","CLUSTER_SET_ACCESS_TYPE_ALLOWED","CLUSTER_SET_ACCESS_TYPE_DENIED","ClusterSetAccountAccess","ClusterSetAccountAccess function [Failover Cluster]","PCLUSTER_SET_ACCOUNT_ACCESS","PCLUSTER_SET_ACCOUNT_ACCESS function [Failover Cluster]","clusapi/ClusterSetAccountAccess","clusapi/PCLUSTER_SET_ACCOUNT_ACCESS","mscs.clustersetaccountaccess"]
old-location: mscs\clustersetaccountaccess.htm
tech.root: MsCS
ms.assetid: E0038A7B-291F-4A30-86BD-D9BD2404D3B5
ms.date: 12/05/2018
ms.keywords: CLUSAPI_ALL_ACCESS, CLUSAPI_CHANGE_ACCESS, CLUSAPI_NO_ACCESS, CLUSAPI_READ_ACCESS, CLUSTER_DELETE_ACCESS_CONTROL_ENTRY, CLUSTER_SET_ACCESS_TYPE_ALLOWED, CLUSTER_SET_ACCESS_TYPE_DENIED, ClusterSetAccountAccess, ClusterSetAccountAccess function [Failover Cluster], PCLUSTER_SET_ACCOUNT_ACCESS, PCLUSTER_SET_ACCOUNT_ACCESS function [Failover Cluster], clusapi/ClusterSetAccountAccess, clusapi/PCLUSTER_SET_ACCOUNT_ACCESS, mscs.clustersetaccountaccess
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
 - ClusterSetAccountAccess
 - clusapi/ClusterSetAccountAccess
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
 - ClusterSetAccountAccess
---

# ClusterSetAccountAccess function


## -description

Updates an account access list (ACL) for a cluster.

## -parameters

### -param hCluster [in]

A handle to the cluster.

### -param szAccountSID [in]

The security identifier (SID) or the account name for the new account access entry (ACE).

### -param dwAccess [in]

The access rights controlled by the ACE.


The possible values are:





#### CLUSAPI_READ_ACCESS (0x00000001L)

Read access.



#### CLUSAPI_CHANGE_ACCESS (0x00000002L)

The account can be used to make changes to the cluster.



#### CLUSAPI_NO_ACCESS (0x00000004L)

No access.



#### CLUSAPI_ALL_ACCESS ((CLUSAPI_READ_ACCESS | CLUSAPI_CHANGE_ACCESS))

The account can be used to read and change the cluster.

### -param dwControlType [in]

The  ACE type to use.


The possible values are:





#### CLUSTER_SET_ACCESS_TYPE_ALLOWED (0)

Adds an allowed ACE.



#### CLUSTER_SET_ACCESS_TYPE_DENIED (1)

Adds a denied ACE.



#### CLUSTER_DELETE_ACCESS_CONTROL_ENTRY (2)

Deletes all the ACEs for the SID.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
      <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-registry-access-functions">Cluster Registry Access Functions</a>
