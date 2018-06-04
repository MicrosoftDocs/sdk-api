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

# _CRYPT_CONTEXT_FUNCTION_PROVIDERS structure


## -description


The <b>CRYPT_CONTEXT_FUNCTION_PROVIDERS</b> structure contains a set of cryptographic function providers for a CNG configuration context.


## -struct-fields




### -field cProviders

The number of elements in the <b>rgpszProviders</b> array.


### -field rgpszProviders

An array of pointers to null-terminated Unicode strings that contain the identifiers of the function providers contained in this set. The <b>cProviders</b> member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/82776e61-03bb-463b-8767-fa4f70fe1341">BCryptEnumContextFunctionProviders</a>
 

 

