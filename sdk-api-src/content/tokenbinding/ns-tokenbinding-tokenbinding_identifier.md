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

# TOKENBINDING_IDENTIFIER structure


## -description


Contains the information for representing a token binding identifier that results from a token binding message exchange.


## -struct-fields




### -field keyType

 




#### - bindingType

The type of the token binding.


#### - hashAlgorithm

The hash algorithm for the token binding. The value of this member is always <b>TOKENBINDING_HASH_ALGORITHM_SHA256</b>.


#### - signatureAlgorithm

The signature algorithm for the token binding. The following values are possible for this member.



#### TOKENBINDING_SIGNATURE_ALGORITHM_RSA (1)



#### TOKENBINDING_SIGNATURE_ALGORITHM_ECDSAP256 (3)


## -see-also




<a href="https://msdn.microsoft.com/6C34E174-CCC4-451D-82C3-C410C8C92C8C">TOKENBINDING_RESULT_DATA</a>
 

 

