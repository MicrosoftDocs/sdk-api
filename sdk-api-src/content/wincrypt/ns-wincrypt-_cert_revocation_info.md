---
UID: NS:wincrypt._CERT_REVOCATION_INFO
title: "_CERT_REVOCATION_INFO"
author: windows-driver-content
description: Indicates the revocation status of a certificate in a CERT_CHAIN_ELEMENT.
old-location: security\cert_revocation_info.htm
old-project: SecCrypto
ms.assetid: 798aa2d7-bf8a-425f-bc36-98a44ba3a9d6
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: "*PCERT_REVOCATION_INFO, CERT_REVOCATION_INFO, CERT_REVOCATION_INFO structure [Security], PCERT_REVOCATION_INFO, PCERT_REVOCATION_INFO structure pointer [Security], _CERT_REVOCATION_INFO, _crypto2_cert_revocation_info, security.cert_revocation_info, wincrypt/CERT_REVOCATION_INFO, wincrypt/PCERT_REVOCATION_INFO"
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
req.typenames: CERT_REVOCATION_INFO, *PCERT_REVOCATION_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CERT_REVOCATION_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CERT_REVOCATION_INFO structure


## -description


The <b>CERT_REVOCATION_INFO</b> structure indicates the revocation status of a certificate in a CERT_CHAIN_ELEMENT.


## -struct-fields




### -field cbSize

Size of this structure in bytes.


### -field dwRevocationResult

Currently defined values are:

<ul>
<li>CERT_TRUST_IS_REVOKED</li>
<li>CERT_TRUST_REVOCATION_STATUS_IS_UNKNOWN</li>
</ul>

### -field pszRevocationOid

Not currently used and is set to <b>NULL</b>.


### -field pvOidSpecificInfo

Not currently used and is set to <b>NULL</b>.


### -field fHasFreshnessTime

BOOL set to <b>TRUE</b> if dwFreshnessTime has been updated.


### -field dwFreshnessTime

If <b>fHasFreshnessTime</b> is <b>TRUE</b>, holds the CurrentTime minus the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list's</a> (CRL's). This time is in seconds.


### -field pCrlInfo

For CRL base revocation checking, a non-<b>NULL</b> pointer to a CERT_REVOCATION_CRL_INFO structure.


## -see-also




<a href="https://msdn.microsoft.com/a1f6ba18-63ef-43ac-a17f-900fa13398aa">CERT_CHAIN_ELEMENT</a>
 

 

