---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

