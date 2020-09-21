---
UID: NS:bcrypt._CRYPT_PROVIDER_REF
title: CRYPT_PROVIDER_REF (bcrypt.h)
description: Contains information about a cryptographic interface that a provider supports.
helpviewer_keywords: ["*PCRYPT_PROVIDER_REF","CRYPT_PROVIDER_REF","CRYPT_PROVIDER_REF structure [Security]","PCRYPT_PROVIDER_REF","PCRYPT_PROVIDER_REF structure pointer [Security]","bcrypt/CRYPT_PROVIDER_REF","bcrypt/PCRYPT_PROVIDER_REF","security.crypt_provider_ref"]
old-location: security\crypt_provider_ref.htm
tech.root: security
ms.assetid: 3bd4a07c-8b80-4bbc-9922-88ea007f6ccd
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_PROVIDER_REF, CRYPT_PROVIDER_REF, CRYPT_PROVIDER_REF structure [Security], PCRYPT_PROVIDER_REF, PCRYPT_PROVIDER_REF structure pointer [Security], bcrypt/CRYPT_PROVIDER_REF, bcrypt/PCRYPT_PROVIDER_REF, security.crypt_provider_ref'
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
req.typenames: CRYPT_PROVIDER_REF, *PCRYPT_PROVIDER_REF
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_PROVIDER_REF
 - bcrypt/_CRYPT_PROVIDER_REF
 - PCRYPT_PROVIDER_REF
 - bcrypt/PCRYPT_PROVIDER_REF
 - CRYPT_PROVIDER_REF
 - bcrypt/CRYPT_PROVIDER_REF
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
 - CRYPT_PROVIDER_REF
---

# CRYPT_PROVIDER_REF structure


## -description

The <b>CRYPT_PROVIDER_REF</b> structure contains information about a cryptographic interface that a provider supports.

## -struct-fields

### -field dwInterface

The identifier of the interface that this reference applies to. This will be one of the <a href="/windows/desktop/SecCNG/cng-interface-identifiers">CNG Interface Identifiers</a>.

### -field pszFunction

A pointer to a null-terminated Unicode string that identifies the algorithm or function that the reference applies to. This can be one of the standard <a href="/windows/desktop/SecCNG/cng-algorithm-identifiers">CNG Algorithm Identifiers</a> or the identifier for another registered algorithm.

### -field pszProvider

A pointer to a null-terminated Unicode string that contains the name of the provider.

### -field cProperties

The number of elements in the <b>rgpProperties</b> array. If the algorithm or function has no properties, then this member will be zero.

### -field rgpProperties

An array of <a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_property_ref">CRYPT_PROPERTY_REF</a> structure pointers that contain the properties for this algorithm or function. The <b>cProperties</b> member contains the number of elements in this array.

### -field pUM

A pointer to a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_image_ref">CRYPT_IMAGE_REF</a> structure that contains information about the user mode provider module. If this information was not requested or the provider is not registered as a user mode provider, this member will be <b>NULL</b>.

### -field pKM

A pointer to a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_image_ref">CRYPT_IMAGE_REF</a> structure that contains information about the kernel mode provider module. If this information was not requested or the provider is not registered as a kernel mode provider, this member will be <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptresolveproviders">BCryptResolveProviders</a>



<a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_provider_refs">CRYPT_PROVIDER_REFS</a>