---
UID: NS:wincrypt._CMSG_SIGNED_ENCODE_INFO
title: CMSG_SIGNED_ENCODE_INFO (wincrypt.h)
description: Contains information to be passed to CryptMsgOpenToEncode if dwMsgType is CMSG_SIGNED.
helpviewer_keywords: ["*PCMSG_SIGNED_ENCODE_INFO","CMSG_SIGNED_ENCODE_INFO","CMSG_SIGNED_ENCODE_INFO structure [Security]","_crypto2_cmsg_signed_encode_info","security.cmsg_signed_encode_info","wincrypt/CMSG_SIGNED_ENCODE_INFO"]
old-location: security\cmsg_signed_encode_info.htm
tech.root: security
ms.assetid: 93138744-8316-461b-908a-1eab47e83f63
ms.date: 12/05/2018
ms.keywords: '*PCMSG_SIGNED_ENCODE_INFO, CMSG_SIGNED_ENCODE_INFO, CMSG_SIGNED_ENCODE_INFO structure [Security], _crypto2_cmsg_signed_encode_info, security.cmsg_signed_encode_info, wincrypt/CMSG_SIGNED_ENCODE_INFO'
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
req.typenames: CMSG_SIGNED_ENCODE_INFO, *PCMSG_SIGNED_ENCODE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMSG_SIGNED_ENCODE_INFO
 - wincrypt/_CMSG_SIGNED_ENCODE_INFO
 - PCMSG_SIGNED_ENCODE_INFO
 - wincrypt/PCMSG_SIGNED_ENCODE_INFO
 - CMSG_SIGNED_ENCODE_INFO
 - wincrypt/CMSG_SIGNED_ENCODE_INFO
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
 - CMSG_SIGNED_ENCODE_INFO
---

# CMSG_SIGNED_ENCODE_INFO structure


## -description

The <b>CMSG_SIGNED_ENCODE_INFO</b> structure contains information to be passed to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a> if <i>dwMsgType</i> is CMSG_SIGNED.

## -struct-fields

### -field cbSize

Size of this structure in bytes.

### -field cSigners

Number of elements in the <b>rgSigners</b> array.

### -field rgSigners

Array of pointers to 
			   <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signer_encode_info">CMSG_SIGNER_ENCODE_INFO</a> structures each holding signer information.

### -field cCertEncoded

Number of elements in the <b>rgCertEncoded</b> array.

### -field rgCertEncoded

Array of pointers to 
              <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_BLOB</a> 
				  structures, each containing an encoded certificate.

### -field cCrlEncoded

Number of elements in the <b>rgCrlEncoded</b> array.

### -field rgCrlEncoded

Array of pointers to 
                <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRL_BLOB</a> structures, each containing an encoded CRL.

### -field cAttrCertEncoded

Number of elements in the <b>rgAttrCertEncoded</b> array.
			 Used only if CMSG_SIGNED_ENCODE_INFO_HAS_CMS_FIELDS is defined.

### -field rgAttrCertEncoded

Array of encoded attribute certificates. 
			 Used only if CMSG_SIGNED_ENCODE_INFO_HAS_CMS_FIELDS is defined. This array of encoded attribute certificates can be used with CMS for PKCS #7 processing.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signer_encode_info">CMSG_SIGNER_ENCODE_INFO</a>



<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>