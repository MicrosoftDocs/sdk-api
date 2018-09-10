---
UID: NS:tokenbinding.TOKENBINDING_IDENTIFIER
title: TOKENBINDING_IDENTIFIER
author: windows-sdk-content
description: Contains the information for representing a token binding identifier that results from a token binding message exchange.
old-location: security\tokenbinding_identifier.htm
tech.root: SecCNG
ms.assetid: 301E099E-B621-41E1-BF9B-3AF8C53F9227
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: TOKENBINDING_IDENTIFIER, TOKENBINDING_IDENTIFIER structure [Security], TOKENBINDING_SIGNATURE_ALGORITHM_ECDSAP256, TOKENBINDING_SIGNATURE_ALGORITHM_RSA, security.tokenbinding_identifier, tokenbinding/TOKENBINDING_IDENTIFIER
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: tokenbinding.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tokenbinding.h
api_name:
 - TOKENBINDING_IDENTIFIER
product: Windows
targetos: Windows
req.typenames: TOKENBINDING_IDENTIFIER
req.redist: 
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
 

 

