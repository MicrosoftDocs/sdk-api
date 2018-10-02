---
UID: NS:wincrypt._CERT_CHAIN_ELEMENT
title: "_CERT_CHAIN_ELEMENT"
author: windows-sdk-content
description: The CERT_CHAIN_ELEMENT structure is a single element in a simple certificate chain.
old-location: security\cert_chain_element.htm
tech.root: seccrypto
ms.assetid: a1f6ba18-63ef-43ac-a17f-900fa13398aa
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: "*PCERT_CHAIN_ELEMENT, CERT_CHAIN_ELEMENT, CERT_CHAIN_ELEMENT structure [Security], PCERT_CHAIN_ELEMENT, PCERT_CHAIN_ELEMENT structure pointer [Security], _CERT_CHAIN_ELEMENT, _crypto2_cert_chain_element, security.cert_chain_element, wincrypt/CERT_CHAIN_ELEMENT, wincrypt/PCERT_CHAIN_ELEMENT"
ms.prod: windows
ms.technology: windows-sdk
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
 - CERT_CHAIN_ELEMENT
product: Windows
targetos: Windows
req.typenames: CERT_CHAIN_ELEMENT, *PCERT_CHAIN_ELEMENT
req.redist: 
---

# _CERT_CHAIN_ELEMENT structure


## -description


The <b>CERT_CHAIN_ELEMENT</b> structure is a single element in a simple certificate chain. Each element has a pointer to a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate context</a>, a pointer to a structure that indicates the error status and information status of the certificate, and a pointer to a structure that indicates the revocation status of the certificate.


## -struct-fields




### -field cbSize

Size of this structure in bytes.


### -field pCertContext

A pointer to a certificate <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a>.


### -field TrustStatus

Structure indicating the status of the certificate. The structure includes an error status code and an information status code. For information about status code values, see CERT_TRUST_STATUS.


### -field pRevocationInfo

A pointer to a CERT_REVOCATION_INFO structure with information on the revocation status of the certificate. If revocation checking was not enabled, <b>pRevocationInfo</b> is <b>NULL</b>.


### -field pIssuanceUsage

A pointer to a CERT_ENHKEY_USAGE structure. If <b>NULL</b>, any issuance policy is acceptable.


### -field pApplicationUsage

A pointer to a CERT_ENHKEY_USAGE structure. If <b>NULL</b>, any enhanced key usage is acceptable.


### -field pwszExtendedErrorInfo

A pointer to a <b>null</b>-terminated wide character string that contains extended error information. If <b>NULL</b>, there is no extended error information.


## -see-also




<a href="https://msdn.microsoft.com/798aa2d7-bf8a-425f-bc36-98a44ba3a9d6">CERT_REVOCATION_INFO</a>



<a href="https://msdn.microsoft.com/c130cab4-bf8d-429a-beb7-04cb5d37d466">CERT_SIMPLE_CHAIN</a>



<a href="https://msdn.microsoft.com/af1e1db2-7b53-4491-8317-4abf3568fb03">CERT_TRUST_STATUS</a>
 

 

