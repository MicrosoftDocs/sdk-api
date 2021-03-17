---
UID: NS:bcrypt._BCRYPT_ALGORITHM_IDENTIFIER
title: BCRYPT_ALGORITHM_IDENTIFIER (bcrypt.h)
description: Is used with the BCryptEnumAlgorithms function to contain a cryptographic algorithm identifier.
helpviewer_keywords: ["BCRYPT_ALGORITHM_IDENTIFIER","BCRYPT_ALGORITHM_IDENTIFIER structure [Security]","bcrypt/BCRYPT_ALGORITHM_IDENTIFIER","security.bcrypt_algorithm_identifier_struct"]
old-location: security\bcrypt_algorithm_identifier_struct.htm
tech.root: security
ms.assetid: a49a21c9-5668-4709-b52a-f6cacd944845
ms.date: 12/05/2018
ms.keywords: BCRYPT_ALGORITHM_IDENTIFIER, BCRYPT_ALGORITHM_IDENTIFIER structure [Security], bcrypt/BCRYPT_ALGORITHM_IDENTIFIER, security.bcrypt_algorithm_identifier_struct
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: BCRYPT_ALGORITHM_IDENTIFIER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BCRYPT_ALGORITHM_IDENTIFIER
 - bcrypt/_BCRYPT_ALGORITHM_IDENTIFIER
 - BCRYPT_ALGORITHM_IDENTIFIER
 - bcrypt/BCRYPT_ALGORITHM_IDENTIFIER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bcrypt.h
api_name:
 - BCRYPT_ALGORITHM_IDENTIFIER
---

# BCRYPT_ALGORITHM_IDENTIFIER structure


## -description

The <b>BCRYPT_ALGORITHM_IDENTIFIER</b> structure is used with the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptenumalgorithms">BCryptEnumAlgorithms</a> function to contain a <a href="/windows/desktop/SecGloss/c-gly">cryptographic algorithm</a> identifier.

## -struct-fields

### -field pszName

A pointer to a null-terminated Unicode string that contains the string identifier of the algorithm. The <a href="/windows/desktop/SecCNG/cng-algorithm-identifiers">CNG Algorithm Identifiers</a> topic contains the predefined algorithm identifiers.

### -field dwClass

Specifies the class of the algorithm. This can be one of the <a href="/windows/desktop/SecCNG/cng-interface-identifiers">CNG Interface Identifiers</a>.

### -field dwFlags

A set of flags that specify other information about the algorithm. There are currently no flags defined for this member.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptenumalgorithms">BCryptEnumAlgorithms</a>