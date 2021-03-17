---
UID: NS:wincrypt._CMC_TAGGED_REQUEST
title: CMC_TAGGED_REQUEST (wincrypt.h)
description: Used in the CMC_DATA_INFO structures to request a certificate.
helpviewer_keywords: ["*PCMC_TAGGED_REQUEST","CMC_TAGGED_REQUEST","CMC_TAGGED_REQUEST structure [Security]","PCMC_TAGGED_REQUEST","PCMC_TAGGED_REQUEST structure pointer [Security]","_crypto2_cmc_tagged_request","security.cmc_tagged_request","wincrypt/CMC_TAGGED_REQUEST","wincrypt/PCMC_TAGGED_REQUEST"]
old-location: security\cmc_tagged_request.htm
tech.root: security
ms.assetid: 425a3f14-8bc9-471d-b11c-1608db473cce
ms.date: 12/05/2018
ms.keywords: '*PCMC_TAGGED_REQUEST, CMC_TAGGED_REQUEST, CMC_TAGGED_REQUEST structure [Security], PCMC_TAGGED_REQUEST, PCMC_TAGGED_REQUEST structure pointer [Security], _crypto2_cmc_tagged_request, security.cmc_tagged_request, wincrypt/CMC_TAGGED_REQUEST, wincrypt/PCMC_TAGGED_REQUEST'
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
req.typenames: CMC_TAGGED_REQUEST, *PCMC_TAGGED_REQUEST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMC_TAGGED_REQUEST
 - wincrypt/_CMC_TAGGED_REQUEST
 - PCMC_TAGGED_REQUEST
 - wincrypt/PCMC_TAGGED_REQUEST
 - CMC_TAGGED_REQUEST
 - wincrypt/CMC_TAGGED_REQUEST
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
 - CMC_TAGGED_REQUEST
---

# CMC_TAGGED_REQUEST structure


## -description

The <b>CMC_TAGGED_REQUEST</b> structure is used in the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmc_data_info">CMC_DATA_INFO</a> structures to request a certificate. In the future, it may be used for other requests.

## -struct-fields

### -field dwTaggedRequestChoice

<b>DWORD</b> identifying the union member to be used. CMC_TAGGED_CERT_REQUEST_CHOICE can be used to select the CMC_TAGGED_CERT_REQUEST.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.pTaggedCertRequest

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmc_tagged_cert_request">CMC_TAGGED_CERT_REQUEST</a> structure containing the signed <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>.

## -remarks

Additional members of the union may be defined in future versions.