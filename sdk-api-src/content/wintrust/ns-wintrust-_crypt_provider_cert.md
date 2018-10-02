---
UID: NS:wintrust._CRYPT_PROVIDER_CERT
title: "_CRYPT_PROVIDER_CERT"
author: windows-sdk-content
description: Provides information about a provider certificate.
old-location: security\crypt_provider_cert.htm
tech.root: seccrypto
ms.assetid: 622e7a72-445a-4820-b236-1c90dad08351
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: "*PCRYPT_PROVIDER_CERT, CERT_CONFIDENCE_AUTHIDEXT, CERT_CONFIDENCE_HIGHEST, CERT_CONFIDENCE_HYGIENE, CERT_CONFIDENCE_SIG, CERT_CONFIDENCE_TIME, CERT_CONFIDENCE_TIMENEST, CRYPT_PROVIDER_CERT, CRYPT_PROVIDER_CERT structure [Security], PCRYPT_PROVIDER_CERT, PCRYPT_PROVIDER_CERT structure pointer [Security], _CRYPT_PROVIDER_CERT, security.crypt_provider_cert, wintrust/CRYPT_PROVIDER_CERT, wintrust/PCRYPT_PROVIDER_CERT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wintrust.h
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
 - Wintrust.h
api_name:
 - CRYPT_PROVIDER_CERT
product: Windows
targetos: Windows
req.typenames: CRYPT_PROVIDER_CERT, *PCRYPT_PROVIDER_CERT
req.redist: 
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
<td width="40%"><a id="CERT_CONFIDENCE_TIMENEST"></a><a id="cert_confidence_timenest"></a><dl>
<dt><b>CERT_CONFIDENCE_TIMENEST</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
The time of the certificate is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CONFIDENCE_AUTHIDEXT"></a><a id="cert_confidence_authidext"></a><dl>
<dt><b>CERT_CONFIDENCE_AUTHIDEXT</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
The authority ID extension is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CONFIDENCE_HYGIENE"></a><a id="cert_confidence_hygiene"></a><dl>
<dt><b>CERT_CONFIDENCE_HYGIENE</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
At a minimum, the signature of the certificate and authority ID extension are valid.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CONFIDENCE_HIGHEST"></a><a id="cert_confidence_highest"></a><dl>
<dt><b>CERT_CONFIDENCE_HIGHEST</b></dt>
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

