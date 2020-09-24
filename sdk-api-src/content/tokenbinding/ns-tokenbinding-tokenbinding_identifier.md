---
UID: NS:tokenbinding.TOKENBINDING_IDENTIFIER
title: TOKENBINDING_IDENTIFIER (tokenbinding.h)
description: Contains the information for representing a token binding identifier that results from a token binding message exchange.
helpviewer_keywords: ["TOKENBINDING_IDENTIFIER","TOKENBINDING_IDENTIFIER structure [Security]","TOKENBINDING_SIGNATURE_ALGORITHM_ECDSAP256","TOKENBINDING_SIGNATURE_ALGORITHM_RSA","security.tokenbinding_identifier","tokenbinding/TOKENBINDING_IDENTIFIER"]
old-location: security\tokenbinding_identifier.htm
tech.root: security
ms.assetid: 301E099E-B621-41E1-BF9B-3AF8C53F9227
ms.date: 12/05/2018
ms.keywords: TOKENBINDING_IDENTIFIER, TOKENBINDING_IDENTIFIER structure [Security], TOKENBINDING_SIGNATURE_ALGORITHM_ECDSAP256, TOKENBINDING_SIGNATURE_ALGORITHM_RSA, security.tokenbinding_identifier, tokenbinding/TOKENBINDING_IDENTIFIER
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
targetos: Windows
req.typenames: TOKENBINDING_IDENTIFIER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TOKENBINDING_IDENTIFIER
 - tokenbinding/TOKENBINDING_IDENTIFIER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tokenbinding.h
api_name:
 - TOKENBINDING_IDENTIFIER
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

<a href="/windows/desktop/api/tokenbinding/ns-tokenbinding-tokenbinding_result_data">TOKENBINDING_RESULT_DATA</a>