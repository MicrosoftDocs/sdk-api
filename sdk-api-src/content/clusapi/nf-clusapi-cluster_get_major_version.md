---
UID: NF:clusapi.CLUSTER_GET_MAJOR_VERSION
title: CLUSTER_GET_MAJOR_VERSION macro
author: windows-sdk-content
description: Extracts the major version portion of a Cluster service version number.
old-location: mscs\cluster_get_major_version.htm
tech.root: mscs
ms.assetid: 674798d9-8614-4e3b-8d9b-cf0d307a7cfc
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: CLUSTER_GET_MAJOR_VERSION, CLUSTER_GET_MAJOR_VERSION macro [Failover Cluster], _wolf_cluster_get_major_version, clusapi/CLUSTER_GET_MAJOR_VERSION, mscs.cluster_get_major_version
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
 - CLUSTER_GET_MAJOR_VERSION
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CLUSTER_GET_MAJOR_VERSION macro


## -description


Extracts the major version portion of a  <a href="https://msdn.microsoft.com/en-us/library/Aa369163(v=VS.85).aspx">Cluster service</a> version number.


## -parameters




### -param _ver

Cluster service version number.


## -remarks



Cluster service version numbers are obtained from the  <a href="https://msdn.microsoft.com/en-us/library/Aa371755(v=VS.85).aspx">NodeHighestVersion</a> and  <a href="https://msdn.microsoft.com/en-us/library/Aa371756(v=VS.85).aspx">NodeLowestVersion</a> properties as well as the function  <a href="https://msdn.microsoft.com/5b259eb9-c5d0-4f4f-8a6b-14eaed716612">GetClusterInformation</a>. For more information, see  <a href="https://msdn.microsoft.com/en-us/library/Aa373117(v=VS.85).aspx">Version Compatibility</a>.

In Windows Server 2016 Minor version has been renamed to upgrade version, but the <a href="https://msdn.microsoft.com/en-us/library/Aa369103(v=VS.85).aspx">CLUSTER_GET_MINOR_VERSION</a> macro remains for compatibility.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa369103(v=VS.85).aspx">CLUSTER_GET_MINOR_VERSION</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt705454(v=VS.85).aspx">CLUSTER_GET_UPGRADE_VERSION</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369105(v=VS.85).aspx">CLUSTER_MAKE_VERSION</a>
 

 

