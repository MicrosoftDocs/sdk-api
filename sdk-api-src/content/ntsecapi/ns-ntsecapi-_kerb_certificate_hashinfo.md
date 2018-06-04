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

# _KERB_CERTIFICATE_HASHINFO structure


## -description


The <b>KERB_CERTIFICATE_HASHINFO</b> structure provides the payload information of the certificate hash.


## -struct-fields




### -field StoreNameLength

Length, in bytes, of the WCHAR string specifying the certificate store name. If <b>StoreNameLength</b> is zero, the "MY" certificate store is implied; otherwise the WCHAR string must immediately follow the <b>KERB_CERTIFICATE_HASHINFO</b> structure in contiguous memory and must include a terminating null character.



### -field HashLength

Length, in bytes, of the certificate hash. The certificate hash data must follow the <b>KERB_CERTIFICATE_HASHINFO</b> structure and certificate store name (if present) in contiguous memory.


