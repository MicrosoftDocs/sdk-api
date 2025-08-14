---
UID: NF:bcrypt.BCRYPT_INIT_AUTH_MODE_INFO
title: BCRYPT_INIT_AUTH_MODE_INFO macro (bcrypt.h)
description: Initializes a BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO structure for use in calls to BCryptEncrypt and BCryptDecrypt functions.
helpviewer_keywords: ["BCRYPT_INIT_AUTH_MODE_INFO","BCRYPT_INIT_AUTH_MODE_INFO macro [Security]","bcrypt/BCRYPT_INIT_AUTH_MODE_INFO","security.bcrypt_init_auth_mode_info"]
old-location: security\bcrypt_init_auth_mode_info.htm
tech.root: security
ms.assetid: 5c825337-bd60-48e4-9d71-bfd1d38ab171
ms.date: 07/01/2025
ms.keywords: BCRYPT_INIT_AUTH_MODE_INFO, BCRYPT_INIT_AUTH_MODE_INFO macro [Security], bcrypt/BCRYPT_INIT_AUTH_MODE_INFO, security.bcrypt_init_auth_mode_info
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BCRYPT_INIT_AUTH_MODE_INFO
 - bcrypt/BCRYPT_INIT_AUTH_MODE_INFO
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
 - BCRYPT_INIT_AUTH_MODE_INFO
---

# BCRYPT_INIT_AUTH_MODE_INFO macro

## -syntax

```cpp
void BCRYPT_INIT_AUTH_MODE_INFO(
    BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO _AUTH_INFO_STRUCT_
);
```


## -description

The <b>BCRYPT_INIT_AUTH_MODE_INFO</b> macro  initializes a <a href="/windows/win32/api/bcrypt/ns-bcrypt-bcrypt_authenticated_cipher_mode_info">BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO</a> structure for use in calls to <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptencrypt">BCryptEncrypt</a> and <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdecrypt">BCryptDecrypt</a> functions.

## -parameters

### -param _AUTH_INFO_STRUCT_

The BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO structure to initialize.
