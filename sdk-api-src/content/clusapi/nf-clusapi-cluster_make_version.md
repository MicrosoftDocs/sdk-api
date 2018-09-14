---
UID: NF:clusapi.CLUSTER_MAKE_VERSION
title: CLUSTER_MAKE_VERSION macro
author: windows-sdk-content
description: Creates a Cluster service version number.
old-location: mscs\cluster_make_version.htm
tech.root: mscs
ms.assetid: 0a53c070-efed-4105-8dce-60647869a93f
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: CLUSTER_MAKE_VERSION, CLUSTER_MAKE_VERSION macro [Failover Cluster], _wolf_cluster_make_version, clusapi/CLUSTER_MAKE_VERSION, mscs.cluster_make_version
ms.prod: windows-hardware
ms.technology: windows-devices
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



Cluster service version numbers are obtained from the  <a href="https://msdn.microsoft.com/en-us/library/Aa371755(v=VS.85).aspx">NodeHighestVersion</a> and  <a href="https://msdn.microsoft.com/en-us/library/Aa371756(v=VS.85).aspx">NodeLowestVersion</a> properties as well as the function  <a href="https://msdn.microsoft.com/5b259eb9-c5d0-4f4f-8a6b-14eaed716612">GetClusterInformation</a>. For more information, see  <a href="https://msdn.microsoft.com/en-us/library/Aa373117(v=VS.85).aspx">Version Compatibility</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa369102(v=VS.85).aspx">CLUSTER_GET_MAJOR_VERSION</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369103(v=VS.85).aspx">CLUSTER_GET_MINOR_VERSION</a>
 

 

