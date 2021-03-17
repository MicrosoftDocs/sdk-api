---
UID: NS:wincrypt._CRYPT_CONTENT_INFO
title: CRYPT_CONTENT_INFO (wincrypt.h)
description: Contains data encoded in the PKCS
helpviewer_keywords: ["*PCRYPT_CONTENT_INFO","CRYPT_CONTENT_INFO","CRYPT_CONTENT_INFO structure [Security]","PCRYPT_CONTENT_INFO","PCRYPT_CONTENT_INFO structure pointer [Security]","_crypto2_crypt_content_info","security.crypt_content_info","wincrypt/CRYPT_CONTENT_INFO","wincrypt/PCRYPT_CONTENT_INFO"]
old-location: security\crypt_content_info.htm
tech.root: security
ms.assetid: 033de6e3-c860-4f41-902b-79f528f5736b
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_CONTENT_INFO, CRYPT_CONTENT_INFO, CRYPT_CONTENT_INFO structure [Security], PCRYPT_CONTENT_INFO, PCRYPT_CONTENT_INFO structure pointer [Security], _crypto2_crypt_content_info, security.crypt_content_info, wincrypt/CRYPT_CONTENT_INFO, wincrypt/PCRYPT_CONTENT_INFO'
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
req.typenames: CRYPT_CONTENT_INFO, *PCRYPT_CONTENT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_CONTENT_INFO
 - wincrypt/_CRYPT_CONTENT_INFO
 - PCRYPT_CONTENT_INFO
 - wincrypt/PCRYPT_CONTENT_INFO
 - CRYPT_CONTENT_INFO
 - wincrypt/CRYPT_CONTENT_INFO
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
 - CRYPT_CONTENT_INFO
---

# CRYPT_CONTENT_INFO structure


## -description

The <b>CRYPT_CONTENT_INFO</b> structure contains data encoded in the PKCS #7 ContentInfo data format.

## -struct-fields

### -field pszObjId

Object identifier (OID) of the type of data contained in the <b>Content</b> member. ContentType in PKCS #7 defines a set of predefined OIDs. However, additional OIDs can be defined and used.

### -field Content

The data encoded in the PKCS #7 ContentInfo data format.

