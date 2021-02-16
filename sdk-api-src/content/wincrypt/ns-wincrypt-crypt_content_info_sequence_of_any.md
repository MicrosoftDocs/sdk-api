---
UID: NS:wincrypt._CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY
title: CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY (wincrypt.h)
description: Contains information representing the Netscape certificate sequence of certificates.
helpviewer_keywords: ["*PCRYPT_CONTENT_INFO_SEQUENCE_OF_ANY","CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY","CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY structure [Security]","PCRYPT_CONTENT_INFO_SEQUENCE_OF_ANY","PCRYPT_CONTENT_INFO_SEQUENCE_OF_ANY structure pointer [Security]","_crypto2_crypt_content_info_sequence_of_any","security.crypt_content_info_sequence_of_any","wincrypt/CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY","wincrypt/PCRYPT_CONTENT_INFO_SEQUENCE_OF_ANY"]
old-location: security\crypt_content_info_sequence_of_any.htm
tech.root: security
ms.assetid: b47cc15d-b92d-4e8a-a8b8-6217d07a0495
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_CONTENT_INFO_SEQUENCE_OF_ANY, CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY, CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY structure [Security], PCRYPT_CONTENT_INFO_SEQUENCE_OF_ANY, PCRYPT_CONTENT_INFO_SEQUENCE_OF_ANY structure pointer [Security], _crypto2_crypt_content_info_sequence_of_any, security.crypt_content_info_sequence_of_any, wincrypt/CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY, wincrypt/PCRYPT_CONTENT_INFO_SEQUENCE_OF_ANY'
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
req.typenames: CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY, *PCRYPT_CONTENT_INFO_SEQUENCE_OF_ANY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY
 - wincrypt/_CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY
 - PCRYPT_CONTENT_INFO_SEQUENCE_OF_ANY
 - wincrypt/PCRYPT_CONTENT_INFO_SEQUENCE_OF_ANY
 - CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY
 - wincrypt/CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY
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
 - CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY
---

# CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY structure


## -description

The <b>CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY</b> structure contains information representing the Netscape certificate sequence of certificates.

A Netscape certificate sequence of certificates can be created by setting the <b>pszObjId</b> member to szOID_NETSCAPE_CERT_SEQUENCE and supplying <a href="/windows/desktop/SecGloss/d-gly">DER</a>-encoded certificates in <b>rgValue</b>.

## -struct-fields

### -field pszObjId

Object identifier (OID) specifying the type of data contained in the <b>rgValue</b> array.

### -field cValue

Number of elements in the <b>rgValue</b> array.

### -field rgValue

Array of pointers to <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DER_BLOB</a> structures. For more information, see 
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>.