---
UID: NS:wincrypt._CRYPT_ENROLLMENT_NAME_VALUE_PAIR
title: CRYPT_ENROLLMENT_NAME_VALUE_PAIR (wincrypt.h)
description: Used to create certificate requests on behalf of a user.
helpviewer_keywords: ["*PCRYPT_ENROLLMENT_NAME_VALUE_PAIR","CRYPT_ENROLLMENT_NAME_VALUE_PAIR","CRYPT_ENROLLMENT_NAME_VALUE_PAIR structure [Security]","_crypto2_crypt_enrollment_name_value_pair","security.crypt_enrollment_name_value_pair","wincrypt/CRYPT_ENROLLMENT_NAME_VALUE_PAIR"]
old-location: security\crypt_enrollment_name_value_pair.htm
tech.root: security
ms.assetid: 996bd28e-73c1-494e-957c-8dd4c7b8e064
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_ENROLLMENT_NAME_VALUE_PAIR, CRYPT_ENROLLMENT_NAME_VALUE_PAIR, CRYPT_ENROLLMENT_NAME_VALUE_PAIR structure [Security], _crypto2_crypt_enrollment_name_value_pair, security.crypt_enrollment_name_value_pair, wincrypt/CRYPT_ENROLLMENT_NAME_VALUE_PAIR'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: CRYPT_ENROLLMENT_NAME_VALUE_PAIR, *PCRYPT_ENROLLMENT_NAME_VALUE_PAIR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_ENROLLMENT_NAME_VALUE_PAIR
 - wincrypt/_CRYPT_ENROLLMENT_NAME_VALUE_PAIR
 - PCRYPT_ENROLLMENT_NAME_VALUE_PAIR
 - wincrypt/PCRYPT_ENROLLMENT_NAME_VALUE_PAIR
 - CRYPT_ENROLLMENT_NAME_VALUE_PAIR
 - wincrypt/CRYPT_ENROLLMENT_NAME_VALUE_PAIR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_ENROLLMENT_NAME_VALUE_PAIR
---

# CRYPT_ENROLLMENT_NAME_VALUE_PAIR structure


## -description

The <b>CRYPT_ENROLLMENT_NAME_VALUE_PAIR</b> structure is used to create certificate requests on behalf of a user.

## -struct-fields

### -field pwszName

Name of a certificate requester.

### -field pwszValue

Name of the user for whom the certificate is being requested.

