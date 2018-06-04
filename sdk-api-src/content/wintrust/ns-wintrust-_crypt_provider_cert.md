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

# _CRYPT_PROVIDER_CERT structure


## -description


<p class="CCE_Message">[The  <b>CRYPT_PROVIDER_CERT</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPT_PROVIDER_CERT</b> structure provides information about a provider certificate.


## -struct-fields




### -field cbStruct

The size, in bytes, of this structure.


### -field pCert

A pointer to the certificate context.


### -field fCommercial

Boolean value that indicates whether the certificate is a commercial certificate.


### -field fTrustedRoot

Boolean value that indicates whether the certificate is a trusted root certificate.


### -field fSelfSigned

Boolean value that indicates whether the certificate is self-signed.


### -field fTestCert

Boolean value that indicates whether the certificate is a test certificate.


### -field dwRevokedReason

Value that specifies the revocation reason, if applicable.


### -field dwConfidence


Bitwise combination of zero or more of the following confidence values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_CONFIDENCE_SIG"></a><a id="cert_confidence_sig"></a><dl>
<dt><b>CERT_CONFIDENCE_SIG</b></dt>
<dt>             0x10000000</dt>
</dl>
</td>
<td width="60%">
The signature of the certificate is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CONFIDENCE_TIME"></a><a id="cert_confidence_time"></a><dl>
<dt><b>CERT_CONFIDENCE_TIME</b></dt>
<dt>            0x01000000</dt>
</dl>
</td>
<td width="60%">
The time of the certificate issuer is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="_CERT_CONFIDENCE_TIMENEST"></a><a id="_cert_confidence_timenest"></a><dl>
<dt><b>
CERT_CONFIDENCE_TIMENEST</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
The time of the certificate is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="_CERT_CONFIDENCE_AUTHIDEXT"></a><a id="_cert_confidence_authidext"></a><dl>
<dt><b>
CERT_CONFIDENCE_AUTHIDEXT</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
The authority ID extension is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="_CERT_CONFIDENCE_HYGIENE"></a><a id="_cert_confidence_hygiene"></a><dl>
<dt><b>
CERT_CONFIDENCE_HYGIENE</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
At a minimum, the signature of the certificate and authority ID extension are valid.

</td>
</tr>
<tr>
<td width="40%"><a id="_CERT_CONFIDENCE_HIGHEST"></a><a id="_cert_confidence_highest"></a><dl>
<dt><b>
CERT_CONFIDENCE_HIGHEST</b></dt>
<dt>0x11111000</dt>
</dl>
</td>
<td width="60%">
Combination of all of the other confidence values.

</td>
</tr>
</table>
 


### -field dwError

A pointer to a <b>DWORD</b> variable that contains the error value for this certificate, if applicable.


### -field pTrustListContext

A pointer to the <a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a> that represents the certificate trust list (CTL).


### -field fTrustListSignerCert

Boolean value that specifies whether the certificate is a trust list signer certificate.


### -field pCtlContext

A pointer to the <a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a> that represents a CTL that contains a self-signed certificate, if applicable.


### -field dwCtlError

A pointer to a <b>DWORD</b> variable that contains the error value for a CTL that contains a self-signed certificate, if applicable.


### -field fIsCyclic

Boolean value that indicates whether the certificate trust is cyclical.


### -field pChainElement

A pointer to the <a href="https://msdn.microsoft.com/a1f6ba18-63ef-43ac-a17f-900fa13398aa">CERT_CHAIN_ELEMENT</a> that represents the status of the certificate within a chain.

