---
UID: NS:wincrypt._CMSG_RC2_AUX_INFO
title: CMSG_RC2_AUX_INFO (wincrypt.h)
description: Contains the bit length of the key for RC2 encryption algorithms.
helpviewer_keywords: ["*PCMSG_RC2_AUX_INFO","CMSG_RC2_AUX_INFO","CMSG_RC2_AUX_INFO structure [Security]","PCMSG_RC2_AUX_INFO","PCMSG_RC2_AUX_INFO structure pointer [Security]","_crypto2_cmsg_rc2_aux_info","security.cmsg_rc2_aux_info","wincrypt/CMSG_RC2_AUX_INFO","wincrypt/PCMSG_RC2_AUX_INFO"]
old-location: security\cmsg_rc2_aux_info.htm
tech.root: security
ms.assetid: 6d7014fa-2d0c-48de-bda5-91d19ad879f9
ms.date: 12/05/2018
ms.keywords: '*PCMSG_RC2_AUX_INFO, CMSG_RC2_AUX_INFO, CMSG_RC2_AUX_INFO structure [Security], PCMSG_RC2_AUX_INFO, PCMSG_RC2_AUX_INFO structure pointer [Security], _crypto2_cmsg_rc2_aux_info, security.cmsg_rc2_aux_info, wincrypt/CMSG_RC2_AUX_INFO, wincrypt/PCMSG_RC2_AUX_INFO'
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
req.typenames: CMSG_RC2_AUX_INFO, *PCMSG_RC2_AUX_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMSG_RC2_AUX_INFO
 - wincrypt/_CMSG_RC2_AUX_INFO
 - PCMSG_RC2_AUX_INFO
 - wincrypt/PCMSG_RC2_AUX_INFO
 - CMSG_RC2_AUX_INFO
 - wincrypt/CMSG_RC2_AUX_INFO
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
 - CMSG_RC2_AUX_INFO
---

# CMSG_RC2_AUX_INFO structure


## -description

The <b>CMSG_RC2_AUX_INFO</b> structure contains the bit length of the key for RC2 encryption algorithms. The <b>pvEncryptionAuxInfo</b> member in <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_enveloped_encode_info">CMSG_ENVELOPED_ENCODE_INFO</a> can be set to point to an instance of this structure.
<div class="alert"><b>Note</b>  This structure is only used when the other members of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_enveloped_encode_info">CMSG_ENVELOPED_ENCODE_INFO</a> structure indicate that a default key length of 40 bits is to be used with an RC2 encryption algorithm. For more information, see 
<b>CMSG_ENVELOPED_ENCODE_INFO</b>.</div><div> </div>

## -struct-fields

### -field cbSize

Size of this structure in bytes.

### -field dwBitLen

Specifies the RC2 effective key length. Currently 40-, 64-, and 128-bit lengths are supported. 




<div class="alert"><b>Note</b>  This value is the actual key bit length to be used. The values of the <b>dwVersion</b> member of a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_rc2_cbc_parameters">CRYPT_RC2_CBC_PARAMETERS</a> structure to indicate the use of a specific key length is not that specific key length. For example, the <b>dwVersion</b> value that indicates the use of a 128-bit key length is CRYPT_RC2_128BIT_VERSION, which is defined as 58, not 128 bits.</div>
<div> </div>
<div class="alert"><b>Note</b>  If <b>dwBitLen</b> is set to CMSG_SP3_COMPATIBLE_ENCRYPT_FLAG, SP3 compatible encryption is done and the 40-bit default length is ignored.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_enveloped_encode_info">CMSG_ENVELOPED_ENCODE_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>