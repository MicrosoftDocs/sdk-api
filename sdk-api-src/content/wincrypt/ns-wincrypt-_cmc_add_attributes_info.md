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

# _CMC_ADD_ATTRIBUTES_INFO structure


## -description


The <b>CMC_ADD_ATTRIBUTES_INFO</b> structure contains certificate attributes to be added to a certificate.


## -struct-fields




### -field dwCmcDataReference

<b>DWORD</b> data reference number.


### -field cCertReference

Count of elements in the <b>rgdwCertReference</b> array.


### -field rgdwCertReference

Array of certificate reference numbers.


### -field cAttribute

Count of the elements in the <b>rgAttribute</b> array.


### -field rgAttribute

Array of pointers to the 
<a href="https://msdn.microsoft.com/cdbaf38d-ddbe-4be0-afbc-f8bd76ef4847">CRYPT_ATTRIBUTE</a> certificate attributes to be added.

