---
UID: NS:wincrypt._OCSP_REQUEST_ENTRY
title: OCSP_REQUEST_ENTRY (wincrypt.h)
description: Contains information about a single certificate in an online certificate status protocol (OCSP) request.
helpviewer_keywords: ["*POCSP_REQUEST_ENTRY","OCSP_REQUEST_ENTRY","OCSP_REQUEST_ENTRY structure [Security]","POCSP_REQUEST_ENTRY","POCSP_REQUEST_ENTRY structure pointer [Security]","security.ocsp_request_entry","wincrypt/OCSP_REQUEST_ENTRY","wincrypt/POCSP_REQUEST_ENTRY"]
old-location: security\ocsp_request_entry.htm
tech.root: security
ms.assetid: 61d5cbc9-22de-4768-b610-138bcd3c9cce
ms.date: 12/05/2018
ms.keywords: '*POCSP_REQUEST_ENTRY, OCSP_REQUEST_ENTRY, OCSP_REQUEST_ENTRY structure [Security], POCSP_REQUEST_ENTRY, POCSP_REQUEST_ENTRY structure pointer [Security], security.ocsp_request_entry, wincrypt/OCSP_REQUEST_ENTRY, wincrypt/POCSP_REQUEST_ENTRY'
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
req.typenames: OCSP_REQUEST_ENTRY, *POCSP_REQUEST_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OCSP_REQUEST_ENTRY
 - wincrypt/_OCSP_REQUEST_ENTRY
 - POCSP_REQUEST_ENTRY
 - wincrypt/POCSP_REQUEST_ENTRY
 - OCSP_REQUEST_ENTRY
 - wincrypt/OCSP_REQUEST_ENTRY
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
 - OCSP_REQUEST_ENTRY
---

# OCSP_REQUEST_ENTRY structure


## -description

The <b>OCSP_REQUEST_ENTRY</b> structure contains information about a single certificate in an <a href="/windows/desktop/SecGloss/o-gly">online certificate status protocol</a> (OCSP) request. This structure populates the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_request_info">OCSP_REQUEST_INFO</a> <b>rgRequestEntry</b> member.

## -struct-fields

### -field CertId

An <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_cert_id">OCSP_CERT_ID</a> structure that specifies the target certificate.

### -field cExtension

The number of elements in the <b>rgExtension</b> array.

### -field rgExtension

An array of pointers to <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a> structures, each of which contains information about the <b>CertId</b> certificate.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_cert_id">OCSP_CERT_ID</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_request_info">OCSP_REQUEST_INFO</a>



<a href="https://www.ietf.org/rfc/rfc2560.txt">RFC 2560  Online Certificate Status Protocol</a>