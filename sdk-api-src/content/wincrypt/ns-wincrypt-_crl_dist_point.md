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

# _CRL_DIST_POINT structure


## -description


The <b>CRL_DIST_POINT</b> structure identifies a single <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) distribution point that a certificate user can reference to determine whether certificates have been revoked. A certificate user can obtain a CRL from an applicable distribution point or can obtain a current complete CRL from the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) directory entry.

The <b>CRL_DIST_POINT</b> structures are the elements in the array member of a 
<a href="https://msdn.microsoft.com/cc0fe49c-80ab-42d8-9756-a6d6b885761e">CRL_DIST_POINTS_INFO</a> structure.


## -struct-fields




### -field DistPointName

A 
						<a href="https://msdn.microsoft.com/f47283c3-34f5-4611-b041-456d28d85dbe">CRL_DIST_POINT_NAME</a> structure that identifies the location of a CRL source. If <b>NULL</b>, the distribution point name defaults to the <b>CRLIssuer</b> name.


### -field ReasonFlags


						A <a href="https://msdn.microsoft.com/6f102ff3-bfff-4415-a5d8-ca2c226074b3">CRYPT_BIT_BLOB</a> that contains a byte that indicates the revocation reasons covered by the CRL. 




If <b>NULL</b>, the indicated CRL distribution point distributes a CRL that will contain an entry for this certificate if this certificate has been revoked, regardless of the revocation reason.

The following are currently defined <b>ReasonFlags</b> values. For revocations of several reasons, combine these <b>ReasonFlags</b> by using a bitwise-<b>OR</b> operation.


<ul>
<li>CRL_REASON_UNUSED_FLAG</li>
<li>CRL_REASON_KEY_COMPROMISE_FLAG</li>
<li>CRL_REASON_CA_COMPROMISE_FLAG</li>
<li>CRL_REASON_AFFILIATION_CHANGED_FLAG</li>
<li>CRL_REASON_SUPERSEDED_FLAG</li>
<li>CRL_REASON_CESSATION_OF_OPERATION_FLAG</li>
<li>CRL_REASON_CERTIFICATE_HOLD_FLAG</li>
</ul>



### -field CRLIssuer

A 
						<a href="https://msdn.microsoft.com/f9a20827-3333-4ce2-b074-2e8ce903fad2">CERT_ALT_NAME_INFO</a> that identifies the authority that issued and signed the CRL. If <b>NULL</b>, the issuer name defaults to the issuer name of the certificate.


## -see-also




<a href="https://msdn.microsoft.com/cc0fe49c-80ab-42d8-9756-a6d6b885761e">CRL_DIST_POINTS_INFO</a>



<a href="https://msdn.microsoft.com/f47283c3-34f5-4611-b041-456d28d85dbe">CRL_DIST_POINT_NAME</a>
 

 

