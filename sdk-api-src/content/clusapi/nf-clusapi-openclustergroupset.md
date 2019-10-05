---
UID: NF:clusapi.OpenClusterGroupSet
title: OpenClusterGroupSet function (clusapi.h)
author: windows-sdk-content
description: Opens a handle to the specified groupset.
old-location: mscs\openclustergroupcollection.htm
tech.root: MsCS
ms.assetid: 8a5b944b-53c2-4437-b580-6ad603d0011a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: OpenClusterGroupSet, OpenClusterGroupSet function [Failover Cluster], PCLUSAPI_OPEN_CLUSTER_GROUP_GROUPSET, PCLUSAPI_OPEN_CLUSTER_GROUP_GROUPSET function [Failover Cluster], clusapi/OpenClusterGroupSet, clusapi/PCLUSAPI_OPEN_CLUSTER_GROUP_GROUPSET, mscs.openclustergroupcollection
ms.topic: function
f1_keywords: 
 - "clusapi/OpenClusterGroupSet"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - OpenClusterGroupSet
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# OpenClusterGroupSet function


## -description


Opens a handle to the specified groupset.


## -parameters




### -param hCluster [in]

A handle to the cluster containing the collection.


### -param lpszGroupSetName [in]

The name of the collection to be opened


## -returns



If the operation succeeds, 
the function returns a groupset handle.

If the operation fails, 
the function returns <b>NULL</b>. For more information about the error, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.



