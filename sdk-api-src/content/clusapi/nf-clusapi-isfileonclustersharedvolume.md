---
UID: NF:clusapi.IsFileOnClusterSharedVolume
title: IsFileOnClusterSharedVolume function (clusapi.h)
description: Specifies whether the file is on the cluster shared volume.
helpviewer_keywords: ["IsFileOnClusterSharedVolume","IsFileOnClusterSharedVolume function [Failover Cluster]","PCLUSAPI_IS_FILE_ON_CLUSTER_SHARED_VOLUME","PCLUSAPI_IS_FILE_ON_CLUSTER_SHARED_VOLUME function [Failover Cluster]","clusapi/IsFileOnClusterSharedVolume","clusapi/PCLUSAPI_IS_FILE_ON_CLUSTER_SHARED_VOLUME","mscs.isfileonclustersharedvolume"]
old-location: mscs\isfileonclustersharedvolume.htm
tech.root: MsCS
ms.assetid: BEE71433-3408-47AA-A7EB-5E212ABC1023
ms.date: 12/05/2018
ms.keywords: IsFileOnClusterSharedVolume, IsFileOnClusterSharedVolume function [Failover Cluster], PCLUSAPI_IS_FILE_ON_CLUSTER_SHARED_VOLUME, PCLUSAPI_IS_FILE_ON_CLUSTER_SHARED_VOLUME function [Failover Cluster], clusapi/IsFileOnClusterSharedVolume, clusapi/PCLUSAPI_IS_FILE_ON_CLUSTER_SHARED_VOLUME, mscs.isfileonclustersharedvolume
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsFileOnClusterSharedVolume
 - clusapi/IsFileOnClusterSharedVolume
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
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
api_name:
 - IsFileOnClusterSharedVolume
---

# IsFileOnClusterSharedVolume function


## -description

Specifies whether the file is on the cluster shared volume.

## -parameters

### -param lpszPathName [in]

A Unicode string that specifies the path of the cluster shared volume. The string ends with a terminating null character.

### -param pbFileIsOnSharedVolume [out]

<b>True</b> if the file is on the cluster shared volume; otherwise <b>false.</b>

## -returns

If the function succeeds, it returns <b>ERROR_SUCCESS</b>.

If the function fails, 
it returns one of the <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-management-functions">Failover Cluster Resource Management Functions</a>