---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CLUSTER_GET_MAJOR_VERSION macro


## -description


Extracts the major version portion of a  <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a> version number.


## -parameters




### -param _ver

Cluster service version number.


## -remarks



Cluster service version numbers are obtained from the  <a href="https://msdn.microsoft.com/915ad936-1bd1-4402-8acc-32a58b8d41d2">NodeHighestVersion</a> and  <a href="https://msdn.microsoft.com/153e0e14-e1b3-458b-bdc7-2ccdb67dabad">NodeLowestVersion</a> properties as well as the function  <a href="https://msdn.microsoft.com/5b259eb9-c5d0-4f4f-8a6b-14eaed716612">GetClusterInformation</a>. For more information, see  <a href="https://msdn.microsoft.com/919345fa-cbaa-4d01-bd3c-9ca69cab5094">Version Compatibility</a>.

In Windows Server 2016 Minor version has been renamed to upgrade version, but the <a href="https://msdn.microsoft.com/90caa255-9b04-4b83-a846-78590bfce3a7">CLUSTER_GET_MINOR_VERSION</a> macro remains for compatibility.




## -see-also




<a href="https://msdn.microsoft.com/90caa255-9b04-4b83-a846-78590bfce3a7">CLUSTER_GET_MINOR_VERSION</a>



<a href="https://msdn.microsoft.com/28C51A05-7BCC-4394-B4D7-505750C045E2">CLUSTER_GET_UPGRADE_VERSION</a>



<a href="https://msdn.microsoft.com/0a53c070-efed-4105-8dce-60647869a93f">CLUSTER_MAKE_VERSION</a>
 

 

