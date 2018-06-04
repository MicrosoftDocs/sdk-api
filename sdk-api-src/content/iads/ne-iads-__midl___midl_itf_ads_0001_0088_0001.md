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

# __MIDL___MIDL_itf_ads_0001_0088_0001 enumeration


## -description


The <b>ADS_PATHTYPE_ENUM</b> enumeration specifies the type of object on which the <a href="https://msdn.microsoft.com/781eda1e-1f13-4bb4-ae8e-c9bf4c08e125">IADsSecurityUtility</a> interface is going to add or modify a security descriptor.


## -enum-fields




### -field ADS_PATH_FILE

Indicates that the security descriptor will be retrieved or set on a file object.


### -field ADS_PATH_FILESHARE

Indicates that the security descriptor will be retrieved or set on a file share object.


### -field ADS_PATH_REGISTRY

Indicates that the security descriptor will be retrieved or set on a registry key object.


## -see-also




<a href="https://msdn.microsoft.com/f0ad5ce5-742d-40dc-ac5a-31d779e40bfd">ADSI Enumerations</a>



<a href="https://msdn.microsoft.com/503247b6-3119-4514-9831-c8f0ef50c0fa">ADS_SD_FORMAT_ENUM</a>



<a href="https://msdn.microsoft.com/781eda1e-1f13-4bb4-ae8e-c9bf4c08e125">IADsSecurityUtility</a>



<a href="https://msdn.microsoft.com/7233a82f-fc38-4718-b674-4e6a00666184">Security Descriptors on Files and Registry Keys</a>
 

 

