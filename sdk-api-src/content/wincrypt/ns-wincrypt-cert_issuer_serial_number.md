---
UID: NS:wincrypt._CERT_ISSUER_SERIAL_NUMBER
title: CERT_ISSUER_SERIAL_NUMBER (wincrypt.h)
description: Acts as a unique identifier of a certificate containing the issuer and issuer's serial number for a certificate.
helpviewer_keywords: ["*PCERT_ISSUER_SERIAL_NUMBER","CERT_ISSUER_SERIAL_NUMBER","CERT_ISSUER_SERIAL_NUMBER structure [Security]","PCERT_ISSUER_SERIAL_NUMBER","PCERT_ISSUER_SERIAL_NUMBER structure pointer [Security]","_crypto2_cert_issuer_serial_number","security.cert_issuer_serial_number","wincrypt/CERT_ISSUER_SERIAL_NUMBER","wincrypt/PCERT_ISSUER_SERIAL_NUMBER"]
old-location: security\cert_issuer_serial_number.htm
tech.root: security
ms.assetid: 4e44113f-81e7-4551-bf4d-50986d6d57bb
ms.date: 12/05/2018
ms.keywords: '*PCERT_ISSUER_SERIAL_NUMBER, CERT_ISSUER_SERIAL_NUMBER, CERT_ISSUER_SERIAL_NUMBER structure [Security], PCERT_ISSUER_SERIAL_NUMBER, PCERT_ISSUER_SERIAL_NUMBER structure pointer [Security], _crypto2_cert_issuer_serial_number, security.cert_issuer_serial_number, wincrypt/CERT_ISSUER_SERIAL_NUMBER, wincrypt/PCERT_ISSUER_SERIAL_NUMBER'
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
req.typenames: CERT_ISSUER_SERIAL_NUMBER, *PCERT_ISSUER_SERIAL_NUMBER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_ISSUER_SERIAL_NUMBER
 - wincrypt/_CERT_ISSUER_SERIAL_NUMBER
 - PCERT_ISSUER_SERIAL_NUMBER
 - wincrypt/PCERT_ISSUER_SERIAL_NUMBER
 - CERT_ISSUER_SERIAL_NUMBER
 - wincrypt/CERT_ISSUER_SERIAL_NUMBER
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
 - CERT_ISSUER_SERIAL_NUMBER
---

# CERT_ISSUER_SERIAL_NUMBER structure


## -description

The <b>CERT_ISSUER_SERIAL_NUMBER</b> structure acts as a unique identifier of a certificate containing the issuer and issuer's serial number for a certificate.

## -struct-fields

### -field Issuer

A <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> structure that contains the name of the issuer.

### -field SerialNumber

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a> structure that contains the serial number of the certificate. The combination of the issuer name and the serial number is a unique identifier of a certificate.