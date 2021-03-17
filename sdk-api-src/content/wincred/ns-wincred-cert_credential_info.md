---
UID: NS:wincred._CERT_CREDENTIAL_INFO
title: CERT_CREDENTIAL_INFO (wincred.h)
description: The CERT_CREDENTIAL_INFO structure contains a reference to a certificate.
helpviewer_keywords: ["*PCERT_CREDENTIAL_INFO","CERT_CREDENTIAL_INFO","CERT_CREDENTIAL_INFO structure [Security]","PCERT_CREDENTIAL_INFO","PCERT_CREDENTIAL_INFO structure pointer [Security]","_cred_cert_credential_info","security.cert_credential_info","wincred/CERT_CREDENTIAL_INFO","wincred/PCERT_CREDENTIAL_INFO"]
old-location: security\cert_credential_info.htm
tech.root: security
ms.assetid: acaa94c3-0562-420a-95c7-44a71374d5ea
ms.date: 12/05/2018
ms.keywords: '*PCERT_CREDENTIAL_INFO, CERT_CREDENTIAL_INFO, CERT_CREDENTIAL_INFO structure [Security], PCERT_CREDENTIAL_INFO, PCERT_CREDENTIAL_INFO structure pointer [Security], _cred_cert_credential_info, security.cert_credential_info, wincred/CERT_CREDENTIAL_INFO, wincred/PCERT_CREDENTIAL_INFO'
req.header: wincred.h
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
req.typenames: CERT_CREDENTIAL_INFO, *PCERT_CREDENTIAL_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_CREDENTIAL_INFO
 - wincred/_CERT_CREDENTIAL_INFO
 - PCERT_CREDENTIAL_INFO
 - wincred/PCERT_CREDENTIAL_INFO
 - CERT_CREDENTIAL_INFO
 - wincred/CERT_CREDENTIAL_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinCred.h
api_name:
 - CERT_CREDENTIAL_INFO
---

# CERT_CREDENTIAL_INFO structure


## -description

The <b>CERT_CREDENTIAL_INFO</b> structure contains a 
    reference to a certificate.

## -struct-fields

### -field cbSize

Size of the structure in bytes. This member should be set to 
      <code>sizeof(CERT_CREDENTIAL_INFO)</code>. This structure might be a larger value in 
      the future, indicating a newer version of the structure.

### -field rgbHashOfCert

SHA-1 hash of the certificate referenced.

## -remarks

<b>CERT_HASH_LENGTH</b> is defined as 20 in WinCred.h.

