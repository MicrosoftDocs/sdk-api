---
UID: NF:clusapi.CLUSTER_MAKE_VERSION
title: CLUSTER_MAKE_VERSION macro (clusapi.h)
author: windows-sdk-content
description: Creates a Cluster service version number.
old-location: mscs\cluster_make_version.htm
tech.root: MsCS
ms.assetid: 0a53c070-efed-4105-8dce-60647869a93f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CLUSTER_MAKE_VERSION, CLUSTER_MAKE_VERSION macro [Failover Cluster], _wolf_cluster_make_version, clusapi/CLUSTER_MAKE_VERSION, mscs.cluster_make_version
ms.topic: macro
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSTER_MAKE_VERSION
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CLUSTER_MAKE_VERSION macro


## -description


Creates a Cluster service version number.


## -parameters




### -param _maj

Major version number.


### -param _min

Minor version number.


## -remarks



Cluster service version numbers are obtained from the  <a href="https://msdn.microsoft.com/915ad936-1bd1-4402-8acc-32a58b8d41d2">NodeHighestVersion</a> and  <a href="https://msdn.microsoft.com/153e0e14-e1b3-458b-bdc7-2ccdb67dabad">NodeLowestVersion</a> properties as well as the function  <a href="https://msdn.microsoft.com/5b259eb9-c5d0-4f4f-8a6b-14eaed716612">GetClusterInformation</a>. For more information, see  <a href="https://msdn.microsoft.com/919345fa-cbaa-4d01-bd3c-9ca69cab5094">Version Compatibility</a>.




## -see-also




<a href="https://msdn.microsoft.com/674798d9-8614-4e3b-8d9b-cf0d307a7cfc">CLUSTER_GET_MAJOR_VERSION</a>



<a href="https://msdn.microsoft.com/90caa255-9b04-4b83-a846-78590bfce3a7">CLUSTER_GET_MINOR_VERSION</a>
 

 

