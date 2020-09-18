---
UID: NF:clusapi.ClusterGroupSetOpenEnum
title: ClusterGroupSetOpenEnum function (clusapi.h)
description: Starts the enumeration of groupset for a cluster.
helpviewer_keywords: ["ClusterGroupSetOpenEnum","ClusterGroupSetOpenEnum function [Failover Cluster]","clusapi/ClusterGroupSetOpenEnum","mscs.clustergroupcollectionopenenum"]
old-location: mscs\clustergroupcollectionopenenum.htm
tech.root: MsCS
ms.assetid: 9e629cc8-2e5f-4682-a9b5-902d13a9792d
ms.date: 12/05/2018
ms.keywords: ClusterGroupSetOpenEnum, ClusterGroupSetOpenEnum function [Failover Cluster], clusapi/ClusterGroupSetOpenEnum, mscs.clustergroupcollectionopenenum
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
 - ClusterGroupSetOpenEnum
 - clusapi/ClusterGroupSetOpenEnum
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
 - ClusterGroupSetOpenEnum
---

# ClusterGroupSetOpenEnum function


## -description

Starts the enumeration of groupset for a cluster.

## -parameters

### -param hCluster [in]

A handle to the cluster containing the groupset.

## -returns

If successful, returns a handle suitable for use with <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clustergroupsetenum">ClusterGroupSetEnum</a>


If the operation fails, 
the function returns <b>NULL</b>. For more information about the error, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.