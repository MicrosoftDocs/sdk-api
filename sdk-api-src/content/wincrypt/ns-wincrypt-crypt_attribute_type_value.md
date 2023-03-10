---
UID: NS:wincrypt._CRYPT_ATTRIBUTE_TYPE_VALUE
title: CRYPT_ATTRIBUTE_TYPE_VALUE (wincrypt.h)
description: Contains a single attribute value. The Value member's CRYPT_OBJID_BLOB is encoded.
helpviewer_keywords: ["*PCRYPT_ATTRIBUTE_TYPE_VALUE","CRYPT_ATTRIBUTE_TYPE_VALUE","CRYPT_ATTRIBUTE_TYPE_VALUE structure [Security]","PCRYPT_ATTRIBUTE_TYPE_VALUE","PCRYPT_ATTRIBUTE_TYPE_VALUE structure pointer [Security]","_crypto2_crypt_attribute_type_value","security.crypt_attribute_type_value","wincrypt/CRYPT_ATTRIBUTE_TYPE_VALUE","wincrypt/PCRYPT_ATTRIBUTE_TYPE_VALUE"]
old-location: security\crypt_attribute_type_value.htm
tech.root: security
ms.assetid: 84057581-d0a9-464a-9399-ba806e37516f
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_ATTRIBUTE_TYPE_VALUE, CRYPT_ATTRIBUTE_TYPE_VALUE, CRYPT_ATTRIBUTE_TYPE_VALUE structure [Security], PCRYPT_ATTRIBUTE_TYPE_VALUE, PCRYPT_ATTRIBUTE_TYPE_VALUE structure pointer [Security], _crypto2_crypt_attribute_type_value, security.crypt_attribute_type_value, wincrypt/CRYPT_ATTRIBUTE_TYPE_VALUE, wincrypt/PCRYPT_ATTRIBUTE_TYPE_VALUE'
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
req.typenames: CRYPT_ATTRIBUTE_TYPE_VALUE, *PCRYPT_ATTRIBUTE_TYPE_VALUE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_ATTRIBUTE_TYPE_VALUE
 - wincrypt/_CRYPT_ATTRIBUTE_TYPE_VALUE
 - PCRYPT_ATTRIBUTE_TYPE_VALUE
 - wincrypt/PCRYPT_ATTRIBUTE_TYPE_VALUE
 - CRYPT_ATTRIBUTE_TYPE_VALUE
 - wincrypt/CRYPT_ATTRIBUTE_TYPE_VALUE
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
 - CRYPT_ATTRIBUTE_TYPE_VALUE
---

# CRYPT_ATTRIBUTE_TYPE_VALUE structure


## -description

The <b>CRYPT_ATTRIBUTE_TYPE_VALUE</b> structure contains a single attribute value. The <b>Value</b> member's <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_OBJID_BLOB</a> is encoded.

## -struct-fields

### -field pszObjId

<a href="/windows/desktop/SecGloss/o-gly">Object identifier</a> (OID) that specifies the attribute type data contained in the <b>Value</b> BLOB.

### -field Value

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_OBJID_BLOB</a> that contains the encoded attribute. The <b>cbData</b> member of the <b>CRYPT_OBJID_BLOB</b> structure indicates the length of the <b>pbData</b> member. The <b>pbData</b> member contains the attribute information.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_alt_name_entry">CERT_ALT_NAME_ENTRY</a>



<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>