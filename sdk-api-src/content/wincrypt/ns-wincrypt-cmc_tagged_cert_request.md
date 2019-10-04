---
UID: NS:wincrypt._CMC_TAGGED_CERT_REQUEST
title: CMC_TAGGED_CERT_REQUEST (wincrypt.h)
author: windows-sdk-content
description: Used in the CMC_TAGGED_REQUEST structure.
old-location: security\cmc_tagged_cert_request.htm
tech.root: SecCrypto
ms.assetid: a90ec8c8-bda5-47a8-a1bb-f70f2eda01b7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PCMC_TAGGED_CERT_REQUEST, CMC_TAGGED_CERT_REQUEST, CMC_TAGGED_CERT_REQUEST structure [Security], PCMC_TAGGED_CERT_REQUEST, PCMC_TAGGED_CERT_REQUEST structure pointer [Security], _crypto2_cmc_tagged_cert_request, security.cmc_tagged_cert_request, wincrypt/CMC_TAGGED_CERT_REQUEST, wincrypt/PCMC_TAGGED_CERT_REQUEST'
ms.topic: struct
f1_keywords:
- wincrypt/CMC_TAGGED_CERT_REQUEST
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Wincrypt.h
api_name:
- CMC_TAGGED_CERT_REQUEST
targetos: Windows
req.typenames: CMC_TAGGED_CERT_REQUEST, *PCMC_TAGGED_CERT_REQUEST
req.redist: 
ms.custom: 19H1
---

# CMC_TAGGED_CERT_REQUEST structure


## -description


The <b>CMC_TAGGED_CERT_REQUEST</b> structure is used in the 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-cmc_tagged_request">CMC_TAGGED_REQUEST</a> structure.


## -struct-fields




### -field dwBodyPartID

<b>DWORD</b> identifying the tagged <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate request</a>.


### -field SignedCertRequest

A <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DER_BLOB</a> structure that contains a signed request for a certificate.

