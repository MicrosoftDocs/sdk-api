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

# _UNIVERSAL_NAME_INFOW structure


## -description


The <b>UNIVERSAL_NAME_INFO</b> structure contains information about the UNC form of a universal name. It is used by the 
<a href="https://msdn.microsoft.com/976b5910-c34f-49fa-b25e-82bf607e33a9">NPGetUniversalName</a> function.


## -struct-fields




### -field lpUniversalName

If the provider supports a universal name, it will return that here.

