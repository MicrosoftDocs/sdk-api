---
UID: NS:wincrypt._CMC_TAGGED_CERT_REQUEST
title: CMC_TAGGED_CERT_REQUEST (wincrypt.h)
description: Used in the CMC_TAGGED_REQUEST structure.
helpviewer_keywords: ["*PCMC_TAGGED_CERT_REQUEST","CMC_TAGGED_CERT_REQUEST","CMC_TAGGED_CERT_REQUEST structure [Security]","PCMC_TAGGED_CERT_REQUEST","PCMC_TAGGED_CERT_REQUEST structure pointer [Security]","_crypto2_cmc_tagged_cert_request","security.cmc_tagged_cert_request","wincrypt/CMC_TAGGED_CERT_REQUEST","wincrypt/PCMC_TAGGED_CERT_REQUEST"]
old-location: security\cmc_tagged_cert_request.htm
tech.root: security
ms.assetid: a90ec8c8-bda5-47a8-a1bb-f70f2eda01b7
ms.date: 12/05/2018
ms.keywords: '*PCMC_TAGGED_CERT_REQUEST, CMC_TAGGED_CERT_REQUEST, CMC_TAGGED_CERT_REQUEST structure [Security], PCMC_TAGGED_CERT_REQUEST, PCMC_TAGGED_CERT_REQUEST structure pointer [Security], _crypto2_cmc_tagged_cert_request, security.cmc_tagged_cert_request, wincrypt/CMC_TAGGED_CERT_REQUEST, wincrypt/PCMC_TAGGED_CERT_REQUEST'
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
req.typenames: CMC_TAGGED_CERT_REQUEST, *PCMC_TAGGED_CERT_REQUEST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMC_TAGGED_CERT_REQUEST
 - wincrypt/_CMC_TAGGED_CERT_REQUEST
 - PCMC_TAGGED_CERT_REQUEST
 - wincrypt/PCMC_TAGGED_CERT_REQUEST
 - CMC_TAGGED_CERT_REQUEST
 - wincrypt/CMC_TAGGED_CERT_REQUEST
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
 - CMC_TAGGED_CERT_REQUEST
---

# CMC_TAGGED_CERT_REQUEST structure


## -description

The <b>CMC_TAGGED_CERT_REQUEST</b> structure is used in the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmc_tagged_request">CMC_TAGGED_REQUEST</a> structure.

## -struct-fields

### -field dwBodyPartID

<b>DWORD</b> identifying the tagged <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>.

### -field SignedCertRequest

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DER_BLOB</a> structure that contains a signed request for a certificate.