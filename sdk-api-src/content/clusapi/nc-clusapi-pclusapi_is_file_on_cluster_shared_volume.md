---
UID: NC:clusapi.PCLUSAPI_IS_FILE_ON_CLUSTER_SHARED_VOLUME
title: PCLUSAPI_IS_FILE_ON_CLUSTER_SHARED_VOLUME
author: windows-sdk-content
description: Specifies whether the file is on the cluster shared volume.
old-location: mscs\isfileonclustersharedvolume.htm
old-project: mscs
ms.assetid: BEE71433-3408-47AA-A7EB-5E212ABC1023
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PCLUSAPI_IS_FILE_ON_CLUSTER_SHARED_VOLUME, PCLUSAPI_IS_FILE_ON_CLUSTER_SHARED_VOLUME callback, PCLUSAPI_IS_FILE_ON_CLUSTER_SHARED_VOLUME callback function [Failover Cluster], clusapi/PCLUSAPI_IS_FILE_ON_CLUSTER_SHARED_VOLUME, mscs.isfileonclustersharedvolume
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: Sources
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ClusAPI.h
api_name:
 - PCLUSAPI_IS_FILE_ON_CLUSTER_SHARED_VOLUME
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_IS_FILE_ON_CLUSTER_SHARED_VOLUME callback function


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
 

 

