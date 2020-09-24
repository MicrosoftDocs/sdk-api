---
UID: NS:bcrypt._BCRYPT_PROVIDER_NAME
title: BCRYPT_PROVIDER_NAME (bcrypt.h)
description: Contains the name of a CNG provider.
helpviewer_keywords: ["BCRYPT_PROVIDER_NAME","BCRYPT_PROVIDER_NAME structure [Security]","bcrypt/BCRYPT_PROVIDER_NAME","security.bcrypt_provider_name_struct"]
old-location: security\bcrypt_provider_name_struct.htm
tech.root: security
ms.assetid: 0c57aa3f-1d9a-4bb2-b142-bce9c054e658
ms.date: 12/05/2018
ms.keywords: BCRYPT_PROVIDER_NAME, BCRYPT_PROVIDER_NAME structure [Security], bcrypt/BCRYPT_PROVIDER_NAME, security.bcrypt_provider_name_struct
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
req.typenames: BCRYPT_PROVIDER_NAME
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BCRYPT_PROVIDER_NAME
 - bcrypt/_BCRYPT_PROVIDER_NAME
 - BCRYPT_PROVIDER_NAME
 - bcrypt/BCRYPT_PROVIDER_NAME
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
 - BCRYPT_PROVIDER_NAME
---

# BCRYPT_PROVIDER_NAME structure


## -description

The <b>BCRYPT_PROVIDER_NAME</b> structure contains the name of a CNG provider.

## -struct-fields

### -field pszProviderName

A pointer to a null-terminated Unicode string that contains the name of the provider.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptenumproviders">BCryptEnumProviders</a>