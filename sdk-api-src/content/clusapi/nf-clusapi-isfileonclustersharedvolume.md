---
UID: NF:clusapi.IsFileOnClusterSharedVolume
title: IsFileOnClusterSharedVolume function (clusapi.h)
author: windows-sdk-content
description: Specifies whether the file is on the cluster shared volume.
old-location: mscs\isfileonclustersharedvolume.htm
tech.root: MsCS
ms.assetid: BEE71433-3408-47AA-A7EB-5E212ABC1023
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IsFileOnClusterSharedVolume, IsFileOnClusterSharedVolume function [Failover Cluster], PCLUSAPI_IS_FILE_ON_CLUSTER_SHARED_VOLUME, PCLUSAPI_IS_FILE_ON_CLUSTER_SHARED_VOLUME function [Failover Cluster], clusapi/IsFileOnClusterSharedVolume, clusapi/PCLUSAPI_IS_FILE_ON_CLUSTER_SHARED_VOLUME, mscs.isfileonclustersharedvolume
ms.topic: function
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
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - IsFileOnClusterSharedVolume
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
it returns one of the <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/d1f7360d-f592-49fb-b3b4-60d93afd7c6f">Failover Cluster Resource Management Functions</a>
 

 

