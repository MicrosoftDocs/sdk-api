---
UID: NF:clusapi.DeleteClusterGroupSet
title: DeleteClusterGroupSet function
author: windows-sdk-content
description: Deletes the specified groupset from the cluster.
old-location: mscs\deleteclustergroupcollection.htm
tech.root: MsCS
ms.assetid: 8787d61b-7a80-404c-985f-1ad4ba01acf0
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DeleteClusterGroupSet, DeleteClusterGroupSet function [Failover Cluster], PCLUSAPI_DELETE_CLUSTER_GROUP_GROUPSET, PCLUSAPI_DELETE_CLUSTER_GROUP_GROUPSET function [Failover Cluster], clusapi/DeleteClusterGroupSet, clusapi/PCLUSAPI_DELETE_CLUSTER_GROUP_GROUPSET, mscs.deleteclustergroupcollection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - DeleteClusterGroupSet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DeleteClusterGroupSet
: 
---

# DeleteClusterGroupSet function


## -description


Deletes the specified groupset from the cluster. The groupset
    must contain no groups.


## -parameters




### -param hGroupSet [in]

A handle to the collection to be deleted


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.



