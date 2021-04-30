---
UID: NS:wincrypt._CRYPT_ATTRIBUTE
title: CRYPT_ATTRIBUTE (wincrypt.h)
description: The CRYPT_ATTRIBUTE structure specifies an attribute that has one or more values.
helpviewer_keywords: ["*PCRYPT_ATTRIBUTE","CRYPT_ATTRIBUTE","CRYPT_ATTRIBUTE structure [Security]","PCRYPT_ATTRIBUTE","PCRYPT_ATTRIBUTE structure pointer [Security]","_crypto2_crypt_attribute","security.crypt_attribute","wincrypt/CRYPT_ATTRIBUTE","wincrypt/PCRYPT_ATTRIBUTE"]
old-location: security\crypt_attribute.htm
tech.root: security
ms.assetid: cdbaf38d-ddbe-4be0-afbc-f8bd76ef4847
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_ATTRIBUTE, CRYPT_ATTRIBUTE, CRYPT_ATTRIBUTE structure [Security], PCRYPT_ATTRIBUTE, PCRYPT_ATTRIBUTE structure pointer [Security], _crypto2_crypt_attribute, security.crypt_attribute, wincrypt/CRYPT_ATTRIBUTE, wincrypt/PCRYPT_ATTRIBUTE'
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
req.typenames: CRYPT_ATTRIBUTE, *PCRYPT_ATTRIBUTE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_ATTRIBUTE
 - wincrypt/_CRYPT_ATTRIBUTE
 - PCRYPT_ATTRIBUTE
 - wincrypt/PCRYPT_ATTRIBUTE
 - CRYPT_ATTRIBUTE
 - wincrypt/CRYPT_ATTRIBUTE
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
 - CRYPT_ATTRIBUTE
---

# CRYPT_ATTRIBUTE structure


## -description

The <b>CRYPT_ATTRIBUTE</b> structure specifies an attribute that has one or more values.

## -struct-fields

### -field pszObjId

An <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) that specifies the type of data contained in the <b>rgValue</b> array.

### -field cValue

A <b>DWORD</b>  value that indicates the number of elements in the <b>rgValue</b> array.

### -field rgValue

Pointer to an array of <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a> structures. The <b>cbData</b> member of the <b>CRYPT_INTEGER_BLOB</b> structure indicates the length of the <b>pbData</b> member. The <b>pbData</b> member contains the attribute information.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_request_info">CERT_REQUEST_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signer_encode_info">CMSG_SIGNER_ENCODE_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attributes">CRYPT_ATTRIBUTES</a>



<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_sign_message_para">CRYPT_SIGN_MESSAGE_PARA</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_time_stamp_request_info">CRYPT_TIME_STAMP_REQUEST_INFO</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindattribute">CertFindAttribute</a>