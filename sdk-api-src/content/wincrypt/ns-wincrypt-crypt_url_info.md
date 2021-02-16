---
UID: NS:wincrypt._CRYPT_URL_INFO
title: CRYPT_URL_INFO (wincrypt.h)
description: Contains information about groupings of URLs.
helpviewer_keywords: ["*PCRYPT_URL_INFO","CRYPT_URL_INFO","CRYPT_URL_INFO structure [Security]","PCRYPT_URL_INFO","PCRYPT_URL_INFO structure pointer [Security]","_crypto2_crypt_url_info","security.crypt_url_info","wincrypt/CRYPT_URL_INFO","wincrypt/PCRYPT_URL_INFO"]
old-location: security\crypt_url_info.htm
tech.root: security
ms.assetid: 58289a66-6580-468c-b001-5da08cf6d4a9
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_URL_INFO, CRYPT_URL_INFO, CRYPT_URL_INFO structure [Security], PCRYPT_URL_INFO, PCRYPT_URL_INFO structure pointer [Security], _crypto2_crypt_url_info, security.crypt_url_info, wincrypt/CRYPT_URL_INFO, wincrypt/PCRYPT_URL_INFO'
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
req.typenames: CRYPT_URL_INFO, *PCRYPT_URL_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_URL_INFO
 - wincrypt/_CRYPT_URL_INFO
 - PCRYPT_URL_INFO
 - wincrypt/PCRYPT_URL_INFO
 - CRYPT_URL_INFO
 - wincrypt/CRYPT_URL_INFO
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
 - CRYPT_URL_INFO
---

# CRYPT_URL_INFO structure


## -description

The <b>CRYPT_URL_INFO</b> structure contains information about groupings of URLs.

## -struct-fields

### -field cbSize

The size, in bytes, of the structure.

### -field dwSyncDeltaTime

Number of seconds between synchronizations.

### -field cGroup

Number of elements in the rgcGroupEntry array of URL groups.

### -field rgcGroupEntry

Array of URL groups returned.

