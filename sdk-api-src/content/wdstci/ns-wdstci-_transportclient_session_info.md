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

# _TRANSPORTCLIENT_SESSION_INFO structure


## -description


This structure is used by the <a href="https://msdn.microsoft.com/36970f1b-9dbf-421f-a078-3da3bbb050e8">PFN_WdsTransportClientSessionStartEx</a> callback function.


## -struct-fields




### -field ulStructureLength

The length of this structure in bytes.


### -field ullFileSize

The size of the file, in bytes.


### -field ulBlockSize

The size of a receive block, in bytes.

