---
UID: NF:clusapi.CLUSTER_GET_MINOR_VERSION
title: CLUSTER_GET_MINOR_VERSION macro
author: windows-sdk-content
description: Extracts the minor version portion of a Cluster service version number.
old-location: mscs\cluster_get_minor_version.htm
tech.root: mscs
ms.assetid: 90caa255-9b04-4b83-a846-78590bfce3a7
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: CLUSTER_GET_MINOR_VERSION, CLUSTER_GET_MINOR_VERSION macro [Failover Cluster], _wolf_cluster_get_minor_version, clusapi/CLUSTER_GET_MINOR_VERSION, mscs.cluster_get_minor_version
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
 - CLUSTER_GET_MINOR_VERSION
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CLUSTER_GET_MINOR_VERSION macro


## -description



Extracts the minor version portion of a  <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a> version number.




## -parameters




### -param _ver

Cluster service version number.


## -remarks



Cluster service version numbers are obtained from the  <a href="https://msdn.microsoft.com/915ad936-1bd1-4402-8acc-32a58b8d41d2">NodeHighestVersion</a> and  <a href="https://msdn.microsoft.com/153e0e14-e1b3-458b-bdc7-2ccdb67dabad">NodeLowestVersion</a> properties as well as the function  <a href="https://msdn.microsoft.com/5b259eb9-c5d0-4f4f-8a6b-14eaed716612">GetClusterInformation</a>. For more information, see  <a href="https://msdn.microsoft.com/919345fa-cbaa-4d01-bd3c-9ca69cab5094">Version Compatibility</a>.

In Windows Server 2016 Minor version has been renamed to upgrade version, but the <b>CLUSTER_GET_MINOR_VERSION</b> macro remains for compatibility.




## -see-also




<a href="https://msdn.microsoft.com/674798d9-8614-4e3b-8d9b-cf0d307a7cfc">CLUSTER_GET_MAJOR_VERSION</a>



<a href="https://msdn.microsoft.com/28C51A05-7BCC-4394-B4D7-505750C045E2">CLUSTER_GET_UPGRADE_VERSION</a>



<a href="https://msdn.microsoft.com/0a53c070-efed-4105-8dce-60647869a93f">CLUSTER_MAKE_VERSION</a>
 

 

