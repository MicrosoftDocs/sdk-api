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

# _SP_INF_SIGNER_INFO_V1_W structure


## -description


The <b>SP_INF_SIGNER_INFO</b> structure stores information about an INF file's digital signature.


## -struct-fields




### -field cbSize

Size of this structure, in bytes.


### -field CatalogFile

Path to the catalog file, stored in an array of maximum size MAX_PATH characters.  


### -field DigitalSigner

Path to the digital signer of the file, stored in an array of maximum size MAX_PATH characters.


### -field DigitalSignerVersion

Version of the digital signer, stored in an array of size MAX_PATH characters.


## -see-also




<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

