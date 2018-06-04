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

# GetIScsiVersionInformation function


## -description


The <b>GetIscsiVersionInformation</b> function retrieves information about the initiator version.


## -parameters




### -param VersionInfo

Pointer to an <a href="https://msdn.microsoft.com/04b9e0c0-2c1e-4553-8eef-697819075bc4">ISCSI_VERSION_INFO</a> structure that contains  initiator version information.


## -returns



Returns <b>ERROR_SUCCESS</b> if the operation is successful. If the operation fails due to a socket connection error, this function will return a Winsock error code.




## -see-also




<a href="https://msdn.microsoft.com/04b9e0c0-2c1e-4553-8eef-697819075bc4">ISCSI_VERSION_INFO</a>
 

 

