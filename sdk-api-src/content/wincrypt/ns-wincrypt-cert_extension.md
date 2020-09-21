---
UID: NS:wincrypt._CERT_EXTENSION
title: CERT_EXTENSION (wincrypt.h)
description: The CERT_EXTENSION structure contains the extension information for a certificate, Certificate Revocation List (CRL) or Certificate Trust List (CTL).
helpviewer_keywords: ["*PCERT_EXTENSION","CERT_EXTENSION","CERT_EXTENSION structure [Security]","PCERT_EXTENSION","PCERT_EXTENSION structure pointer [Security]","_crypto2_cert_extension","security.cert_extension","wincrypt/CERT_EXTENSION","wincrypt/PCERT_EXTENSION"]
old-location: security\cert_extension.htm
tech.root: security
ms.assetid: 787a4df0-c0e3-46b9-a7e6-eb3bee3ed717
ms.date: 12/05/2018
ms.keywords: '*PCERT_EXTENSION, CERT_EXTENSION, CERT_EXTENSION structure [Security], PCERT_EXTENSION, PCERT_EXTENSION structure pointer [Security], _crypto2_cert_extension, security.cert_extension, wincrypt/CERT_EXTENSION, wincrypt/PCERT_EXTENSION'
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
req.typenames: CERT_EXTENSION, *PCERT_EXTENSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_EXTENSION
 - wincrypt/_CERT_EXTENSION
 - PCERT_EXTENSION
 - wincrypt/PCERT_EXTENSION
 - CERT_EXTENSION
 - wincrypt/CERT_EXTENSION
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
 - CERT_EXTENSION
---

# CERT_EXTENSION structure


## -description

The <b>CERT_EXTENSION</b> structure contains the extension information for a <a href="/windows/desktop/SecGloss/c-gly">certificate</a>, <a href="/windows/desktop/SecGloss/c-gly">Certificate Revocation List</a> (CRL) or <a href="/windows/desktop/SecGloss/c-gly">Certificate Trust List</a> (CTL).

## -struct-fields

### -field pszObjId

<a href="/windows/desktop/SecGloss/o-gly">Object identifier</a> (OID) that specifies the structure of the extension data contained in the <b>Value</b> member. For specifics on extension OIDs and their related structures, see 
<a href="/windows/desktop/SecCrypto/cryptography-structures">X.509 Certificate Extension Structures</a>.

### -field fCritical

If <b>TRUE</b>, any limitations specified by the extension in the <b>Value</b> member of this structure are imperative. If <b>FALSE</b>, limitations set by this extension can be ignored.

### -field Value

A 
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_OBJID_BLOB</a> structure that contains the encoded extension data. The <b>cbData</b> member of <b>Value</b> indicates the length in bytes of the <b>pbData</b> member. The <b>pbData</b> member byte string is the encoded extension.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extensions">CERT_EXTENSIONS</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_entry">CRL_ENTRY</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_info">CRL_INFO</a>



<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_entry">CTL_ENTRY</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_info">CTL_INFO</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindextension">CertFindExtension</a>