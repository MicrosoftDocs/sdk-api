---
UID: NS:wincrypt._CMC_TAGGED_REQUEST
title: "_CMC_TAGGED_REQUEST"
author: windows-driver-content
description: Used in the CMC_DATA_INFO structures to request a certificate.
old-location: security\cmc_tagged_request.htm
old-project: SecCrypto
ms.assetid: 425a3f14-8bc9-471d-b11c-1608db473cce
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: "*PCMC_TAGGED_REQUEST, CMC_TAGGED_REQUEST, CMC_TAGGED_REQUEST structure [Security], PCMC_TAGGED_REQUEST, PCMC_TAGGED_REQUEST structure pointer [Security], _CMC_TAGGED_REQUEST, _crypto2_cmc_tagged_request, security.cmc_tagged_request, wincrypt/CMC_TAGGED_REQUEST, wincrypt/PCMC_TAGGED_REQUEST"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: CMC_TAGGED_REQUEST, *PCMC_TAGGED_REQUEST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CMC_TAGGED_REQUEST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CMC_TAGGED_REQUEST structure


## -description


The <b>CMC_TAGGED_REQUEST</b> structure is used in the 
<a href="https://msdn.microsoft.com/6245af5a-7a19-4665-bf6c-ad803998d840">CMC_DATA_INFO</a> structures to request a certificate. In the future, it may be used for other requests.


## -struct-fields




### -field dwTaggedRequestChoice

<b>DWORD</b> identifying the union member to be used. CMC_TAGGED_CERT_REQUEST_CHOICE can be used to select the CMC_TAGGED_CERT_REQUEST.


### -field DUMMYUNIONNAME

 




#### - pTaggedCertRequest

A pointer to a 
<a href="https://msdn.microsoft.com/a90ec8c8-bda5-47a8-a1bb-f70f2eda01b7">CMC_TAGGED_CERT_REQUEST</a> structure containing the signed <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>.


## -remarks



Additional members of the union may be defined in future versions.



