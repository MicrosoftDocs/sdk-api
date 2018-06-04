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

# _HTTPAPI_VERSION structure


## -description


The 
<b>HTTPAPI_VERSION</b> structure defines the version of the HTTP Server API. This is not to be confused with the version of the HTTP protocol used, which is stored in an 
<b>HTTP_VERSION</b> structure.


## -struct-fields




### -field HttpApiMajorVersion

Major version of the HTTP Server API.


### -field HttpApiMinorVersion

Minor version of the HTTP Server API.


## -remarks



Constants that represents the version of the API  are pre-defined in the Http.h header file as follows:

"#define HTTPAPI_VERSION_1 {1, 0}"

"#define HTTPAPI_VERSION_2 {2, 0}"



