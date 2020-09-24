---
UID: NS:wincrypt._CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO
title: CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO (wincrypt.h)
description: Contains optional extra information that can be passed to the CryptGetTimeValidObject function in the pExtraInfo parameter.
helpviewer_keywords: ["*PCRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO","CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO","CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO structure [Security]","PCRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO","PCRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO structure pointer [Security]","security.crypt_get_time_valid_object_extra_info","wincrypt/CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO","wincrypt/PCRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO"]
old-location: security\crypt_get_time_valid_object_extra_info.htm
tech.root: security
ms.assetid: 3de595f9-c922-4c8f-8328-819e91a2997c
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO, CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO, CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO structure [Security], PCRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO, PCRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO structure pointer [Security], security.crypt_get_time_valid_object_extra_info, wincrypt/CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO, wincrypt/PCRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO'
req.header: wincrypt.h
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
req.typenames: CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO, *PCRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO
 - wincrypt/_CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO
 - PCRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO
 - wincrypt/PCRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO
 - CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO
 - wincrypt/CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO
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
 - CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO
---

# CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO structure


## -description

 The <b>CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO</b> structure contains optional extra information that can be passed to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgettimevalidobject">CryptGetTimeValidObject</a> function in the <i>pExtraInfo</i> parameter.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field iDeltaCrlIndicator

A value used to compare to the base <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) number. If the base CRL number is less than this value, the caller should attempt to retrieve a newer base CRL.

If the <b>pDeltaCrlIndicator</b> member is non-<b>NULL</b>  the value of this member must be 0x7fffffff.<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>Because the <b>pDeltaCrlIndicator</b> member does not exist, the  <b>iDeltaCrlIndicator</b> value requirement does not apply.

### -field pftCacheResync

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that governs the use of cached information. Any information cached  before this time is considered invalid and new information is retrieved.

### -field pLastSyncTime

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the time of the last synchronization of the data retrieved for the object.

### -field pMaxAgeTime

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that specifies an expiration time of the data retrieved based on the <b>dwMaxAge</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cryptnet_url_cache_response_info">CRYPTNET_URL_CACHE_RESPONSE_INFO</a> structure.

### -field pChainPara

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_revocation_chain_para">CERT_REVOCATION_CHAIN_PARA</a> structure that contains the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain">CertGetCertificateChain</a> function parameters used by the caller. The data in this member enables independent <a href="/windows/desktop/SecGloss/o-gly">online certificate status protocol</a> (OCSP) signer certificate chain verification.

### -field pDeltaCrlIndicator

A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a> structure that contains a CRL with a length of more than 4 bytes. If this member is  non-<b>NULL</b> and the <b>iDeltaCrlIndicator</b> member is equal to <b>MAXLONG</b>, then if the base CRL number is less than this value, the caller should attempt to retrieve a newer base CRL.


<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This member is not supported.

## -remarks

All members of the <b>CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO</b> structure that do not have a value must be set to zero.