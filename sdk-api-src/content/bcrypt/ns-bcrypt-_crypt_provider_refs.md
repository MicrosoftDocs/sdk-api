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

# _CRYPT_PROVIDER_REFS structure


## -description


The <b>CRYPT_PROVIDER_REFS</b> structure contains a collection of provider references.


## -struct-fields




### -field cProviders

The number of elements in the <b>rgpProviders</b> array.


### -field rgpProviders

An array of <a href="https://msdn.microsoft.com/3bd4a07c-8b80-4bbc-9922-88ea007f6ccd">CRYPT_PROVIDER_REF</a> structure pointers that contain the provider references. The <b>cProviders</b> member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/cf30f635-4918-4911-9db0-df90d26a2f1a">BCryptResolveProviders</a>
 

 

