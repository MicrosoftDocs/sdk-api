---
UID: NS:bcrypt._CRYPT_PROPERTY_REF
title: CRYPT_PROPERTY_REF (bcrypt.h)
description: Contains information about a CNG context property.
helpviewer_keywords: ["*PCRYPT_PROPERTY_REF","CRYPT_PROPERTY_REF","CRYPT_PROPERTY_REF structure [Security]","PCRYPT_PROPERTY_REF","PCRYPT_PROPERTY_REF structure pointer [Security]","bcrypt/CRYPT_PROPERTY_REF","bcrypt/PCRYPT_PROPERTY_REF","security.crypt_property_ref"]
old-location: security\crypt_property_ref.htm
tech.root: security
ms.assetid: 450225b8-87f2-4ce2-853d-e78cf64bd13d
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_PROPERTY_REF, CRYPT_PROPERTY_REF, CRYPT_PROPERTY_REF structure [Security], PCRYPT_PROPERTY_REF, PCRYPT_PROPERTY_REF structure pointer [Security], bcrypt/CRYPT_PROPERTY_REF, bcrypt/PCRYPT_PROPERTY_REF, security.crypt_property_ref'
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
req.typenames: CRYPT_PROPERTY_REF, *PCRYPT_PROPERTY_REF
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_PROPERTY_REF
 - bcrypt/_CRYPT_PROPERTY_REF
 - PCRYPT_PROPERTY_REF
 - bcrypt/PCRYPT_PROPERTY_REF
 - CRYPT_PROPERTY_REF
 - bcrypt/CRYPT_PROPERTY_REF
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
 - CRYPT_PROPERTY_REF
---

# CRYPT_PROPERTY_REF structure


## -description

The <b>CRYPT_PROPERTY_REF</b> structure contains information about a CNG context property.

## -struct-fields

### -field pszProperty

A pointer to a null-terminated Unicode string that contains the name of the property.

### -field cbValue

The size, in bytes, of the <b>pbValue</b> buffer.

### -field pbValue

A pointer to a memory buffer that contains the value of the property. The format and type of this data depend on the property.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptresolveproviders">BCryptResolveProviders</a>



<a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_provider_ref">CRYPT_PROVIDER_REF</a>