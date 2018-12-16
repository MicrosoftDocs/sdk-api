---
UID: NS:wincrypt._CMC_TAGGED_CERT_REQUEST
title: CMC_TAGGED_CERT_REQUEST
author: windows-sdk-content
description: Used in the CMC_TAGGED_REQUEST structure.
old-location: security\cmc_tagged_cert_request.htm
tech.root: seccrypto
ms.assetid: a90ec8c8-bda5-47a8-a1bb-f70f2eda01b7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCMC_TAGGED_CERT_REQUEST, CMC_TAGGED_CERT_REQUEST, CMC_TAGGED_CERT_REQUEST structure [Security], PCMC_TAGGED_CERT_REQUEST, PCMC_TAGGED_CERT_REQUEST structure pointer [Security], _crypto2_cmc_tagged_cert_request, security.cmc_tagged_cert_request, wincrypt/CMC_TAGGED_CERT_REQUEST, wincrypt/PCMC_TAGGED_CERT_REQUEST"
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: CMC_TAGGED_CERT_REQUEST, *PCMC_TAGGED_CERT_REQUEST
req.redist: 
---

# CMC_TAGGED_CERT_REQUEST structure


## -description


The <b>CMC_TAGGED_CERT_REQUEST</b> structure is used in the 
<a href="https://msdn.microsoft.com/425a3f14-8bc9-471d-b11c-1608db473cce">CMC_TAGGED_REQUEST</a> structure.


## -struct-fields




### -field dwBodyPartID

<b>DWORD</b> identifying the tagged <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>.


### -field SignedCertRequest

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DER_BLOB</a> structure that contains a signed request for a certificate.

