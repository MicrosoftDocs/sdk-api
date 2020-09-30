---
UID: NS:wincrypt._OCSP_REQUEST_INFO
title: OCSP_REQUEST_INFO (wincrypt.h)
description: Contains information for an online certificate status protocol (OCSP) request as specified by RFC 2560.
helpviewer_keywords: ["*POCSP_REQUEST_INFO","OCSP_REQUEST_INFO","OCSP_REQUEST_INFO structure [Security]","OCSP_REQUEST_V1","POCSP_REQUEST_INFO","POCSP_REQUEST_INFO structure pointer [Security]","security.ocsp_request_info","wincrypt/OCSP_REQUEST_INFO","wincrypt/POCSP_REQUEST_INFO"]
old-location: security\ocsp_request_info.htm
tech.root: security
ms.assetid: ec939c3b-f155-45f2-b507-6c2e6069a868
ms.date: 12/05/2018
ms.keywords: '*POCSP_REQUEST_INFO, OCSP_REQUEST_INFO, OCSP_REQUEST_INFO structure [Security], OCSP_REQUEST_V1, POCSP_REQUEST_INFO, POCSP_REQUEST_INFO structure pointer [Security], security.ocsp_request_info, wincrypt/OCSP_REQUEST_INFO, wincrypt/POCSP_REQUEST_INFO'
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
req.typenames: OCSP_REQUEST_INFO, *POCSP_REQUEST_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OCSP_REQUEST_INFO
 - wincrypt/_OCSP_REQUEST_INFO
 - POCSP_REQUEST_INFO
 - wincrypt/POCSP_REQUEST_INFO
 - OCSP_REQUEST_INFO
 - wincrypt/OCSP_REQUEST_INFO
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
 - OCSP_REQUEST_INFO
---

# OCSP_REQUEST_INFO structure


## -description

The <b>OCSP_REQUEST_INFO</b> structure contains information for an  <a href="/windows/desktop/SecGloss/o-gly">online certificate status protocol</a> (OCSP) request as specified by <a href="https://www.ietf.org/rfc/rfc2560.txt">RFC 2560</a>. The RFC specifies that a single request can contain a sequence of certificates for which statuses are required. The  <b>rgRequestEntry</b> member of this structure contains an <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_request_entry">OCSP_REQUEST_ENTRY</a> structure for each certificate in a sequence.

## -struct-fields

### -field dwVersion

A value that indicates the protocol version of the OCSP request.



#### OCSP_REQUEST_V1 (0)

### -field pRequestorName

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_alt_name_entry">CERT_ALT_NAME_ENTRY</a> structure that contains the name bound to the certificate <a href="/windows/desktop/SecGloss/p-gly">public key</a> of the requester.

### -field cRequestEntry

The number of elements in the <b>rgRequestEntry</b> array.

### -field rgRequestEntry

An array of pointers to <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_request_entry">OCSP_REQUEST_ENTRY</a> structures.

### -field cExtension

The number of elements in the <b>rgExtension</b> array.

### -field rgExtension

An array of pointers to <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a> structures, each of which contains information about the request.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_alt_name_entry">CERT_ALT_NAME_ENTRY</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_request_entry">OCSP_REQUEST_ENTRY</a>



<a href="https://www.ietf.org/rfc/rfc2560.txt">RFC 2560 Online Certificate Status Protocol</a>