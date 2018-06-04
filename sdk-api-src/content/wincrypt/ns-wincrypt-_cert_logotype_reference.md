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

# _CERT_LOGOTYPE_REFERENCE structure


## -description


The <b>CERT_LOGOTYPE_REFERENCE</b> structure contains logotype reference information.


## -struct-fields




### -field cHashedUrl

The number of elements in the <b>rgHashedUrl</b> array.


### -field rgHashedUrl

An array of <a href="https://msdn.microsoft.com/961feb88-b924-4834-bc68-d87f410259f1">CERT_HASHED_URL</a> structures that contain the hashed URL of the logotype. The <b>cHashedUrl</b> member contains the number of elements in this array.

