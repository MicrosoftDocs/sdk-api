---
UID: NS:wincrypt._CRL_ENTRY
title: CRL_ENTRY (wincrypt.h)
description: Contains information about a single revoked certificate. It is a member of a CRL_INFO structure.
helpviewer_keywords: ["*PCRL_ENTRY","CRL_ENTRY","CRL_ENTRY structure [Security]","PCRL_ENTRY","PCRL_ENTRY structure pointer [Security]","_crypto2_crl_entry","security.crl_entry","wincrypt/CRL_ENTRY","wincrypt/PCRL_ENTRY"]
old-location: security\crl_entry.htm
tech.root: security
ms.assetid: 30e7952a-a408-404f-9058-8197539387f6
ms.date: 12/05/2018
ms.keywords: '*PCRL_ENTRY, CRL_ENTRY, CRL_ENTRY structure [Security], PCRL_ENTRY, PCRL_ENTRY structure pointer [Security], _crypto2_crl_entry, security.crl_entry, wincrypt/CRL_ENTRY, wincrypt/PCRL_ENTRY'
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
req.typenames: CRL_ENTRY, *PCRL_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRL_ENTRY
 - wincrypt/_CRL_ENTRY
 - PCRL_ENTRY
 - wincrypt/PCRL_ENTRY
 - CRL_ENTRY
 - wincrypt/CRL_ENTRY
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
 - CRL_ENTRY
---

# CRL_ENTRY structure


## -description

The <b>CRL_ENTRY</b> structure contains information about a single revoked certificate. It is a member of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_info">CRL_INFO</a> structure.

## -struct-fields

### -field SerialNumber

A <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> that contains the serial number of a <a href="/windows/desktop/SecGloss/c-gly">revoked certificate</a>. 




Leading 0x00 or 0xFF bytes are removed. For more information, see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcompareintegerblob">CertCompareIntegerBlob</a>.

### -field RevocationDate

Date that the certificate was revoked. Time is UTC-time encoded as an eight-byte date/time precise to seconds with a two digit year (that is, YYMMDDHHMMSS plus 2 bytes). The date is interpreted as a date between the years 1968 and 2067.

### -field cExtension

Number of elements in the <b>rgExtension</b> member array of extensions.

### -field rgExtension

Array of pointers to 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a> structures, each providing information about the revoked certificate.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_info">CRL_INFO</a>



<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>