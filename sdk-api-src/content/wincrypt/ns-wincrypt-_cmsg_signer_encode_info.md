---
UID: NS:wincrypt._CMSG_SIGNER_ENCODE_INFO
title: "_CMSG_SIGNER_ENCODE_INFO"
author: windows-sdk-content
description: Contains signer information. It is passed to CryptMsgCountersign, CryptMsgCountersignEncoded, and optionally to CryptMsgOpenToEncode as a member of the CMSG_SIGNED_ENCODE_INFO structure, if the dwMsgType parameter is CMSG_SIGNED.
old-location: security\cmsg_signer_encode_info.htm
old-project: seccrypto
ms.assetid: f599226d-ddd7-455f-b650-74b91674d8f9
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: "*PCMSG_SIGNER_ENCODE_INFO, AT_KEYEXCHANGE, AT_SIGNATURE, CMSG_SIGNER_ENCODE_INFO, CMSG_SIGNER_ENCODE_INFO structure [Security], PCMSG_SIGNER_ENCODE_INFO, PCMSG_SIGNER_ENCODE_INFO structure pointer [Security], _CMSG_SIGNER_ENCODE_INFO, _crypto2_cmsg_signer_encode_info, security.cmsg_signer_encode_info, wincrypt/CMSG_SIGNER_ENCODE_INFO, wincrypt/PCMSG_SIGNER_ENCODE_INFO"
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
tech.root: 
req.typenames: CMSG_SIGNER_ENCODE_INFO, *PCMSG_SIGNER_ENCODE_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CMSG_SIGNER_ENCODE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CMSG_SIGNER_ENCODE_INFO structure


## -description


The <b>CMSG_SIGNER_ENCODE_INFO</b> structure contains signer information. It is passed to 
<a href="https://msdn.microsoft.com/ebf76664-bca6-462d-b519-2b60f435d8ef">CryptMsgCountersign</a>, 
<a href="https://msdn.microsoft.com/d9fd734b-e14d-4392-ac88-5565aefbedb4">CryptMsgCountersignEncoded</a>, and optionally to 
<a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a> as a member of 
the <a href="https://msdn.microsoft.com/93138744-8316-461b-908a-1eab47e83f63">CMSG_SIGNED_ENCODE_INFO</a> structure, if the <i>dwMsgType</i> parameter is CMSG_SIGNED.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field pCertInfo

A pointer to a 
<a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a> structure that contains the  


<b>Issuer</b>, <b>SerialNumber</b>, and <b>SubjectPublicKeyInfo</b> members.

The <b>pbData</b> members of the <b>Issuer</b> and <b>SerialNumber</b> structures combined uniquely identify a certificate. The <b>Algorithm</b> member of the <b>SubjectPublicKeyInfo</b> structure specifies the <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> encryption algorithm used.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.hCryptProv

A handle to the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP).
If <b>HashEncryptionAlgorithm</b> is set to szOID_PKIX_NO_SIGNATURE, this handle can be the handle of a CSP acquired by using the <i>dwFlags</i> parameter set to <b>CRYPT_VERIFYCONTEXT</b>. The CNG function <a href="https://msdn.microsoft.com/ad841c2e-8097-4b07-914e-8e7240d55585">NCryptIsKeyHandle</a> is called to determine the union choice.


### -field DUMMYUNIONNAME.hNCryptKey

A handle to the CNG CSP. The CNG function <a href="https://msdn.microsoft.com/ad841c2e-8097-4b07-914e-8e7240d55585">NCryptIsKeyHandle</a> is called to determine the union choice. New encrypt algorithms are only supported in CNG functions. The CNG function <a href="https://msdn.microsoft.com/0c339864-b598-430c-a597-09d3571fdbb2">NCryptTranslateHandle</a> will be called to convert the CryptoAPI <i>hCryptProv</i> choice where necessary. We recommend that applications pass, to the <i>hNCryptKey</i> member, the CNG CSP handle that is returned from the <a href="https://msdn.microsoft.com/581c5d89-730d-4d8c-b3bb-a28edec25910">NCryptOpenKey</a> function.


### -field DUMMYUNIONNAME.hBCryptKey

 


### -field dwKeySpec

Specifies the private key to be used. This member is not used when the <i>hNCryptKey</i> member is used. 




If <b>dwKeySpec</b> is zero, then the default AT_KEYEXCHANGE value is used.

The following <b>dwKeySpec</b> values are defined for the default provider.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AT_KEYEXCHANGE"></a><a id="at_keyexchange"></a><dl>
<dt><b>AT_KEYEXCHANGE</b></dt>
</dl>
</td>
<td width="60%">
Keys used to encrypt/decrypt session keys.

</td>
</tr>
<tr>
<td width="40%"><a id="AT_SIGNATURE"></a><a id="at_signature"></a><dl>
<dt><b>AT_SIGNATURE</b></dt>
</dl>
</td>
<td width="60%">
Keys used to create and verify digital signatures.

</td>
</tr>
</table>
 


### -field HashAlgorithm

A 
						<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that specifies the hash algorithm.


### -field pvHashAuxInfo

Not used. This member must be set to <b>NULL</b>.


### -field cAuthAttr

The number of elements in the <b>rgAuthAttr</b> array. If no authenticated attributes are present in <b>rgAuthAttr</b>, then <b>cAuthAttr</b> is zero.


### -field rgAuthAttr

An array of pointers to 
<a href="https://msdn.microsoft.com/cdbaf38d-ddbe-4be0-afbc-f8bd76ef4847">CRYPT_ATTRIBUTE</a> structures, each of which contains authenticated attribute information. 




The PKCS #9 standard dictates that if there are any attributes, there must be at least two: the content type <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) and the hash of the message. These attributes are automatically added by the system.


### -field cUnauthAttr

The number of elements in the <b>rgUnauthAttr</b> array. If there are no unauthenticated attributes, <b>cUnauthAttr</b> is zero.


### -field rgUnauthAttr

An array of pointers to <a href="https://msdn.microsoft.com/cdbaf38d-ddbe-4be0-afbc-f8bd76ef4847">CRYPT_ATTRIBUTE</a> structures, each of which contains unauthenticated attribute information. Unauthenticated attributes can contain <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">countersignatures</a>, among other uses.


### -field SignerId


						A <a href="https://msdn.microsoft.com/9e33f661-c365-4725-8c3f-27b6cdd9a84e">CERT_ID</a> structure that contains a unique identifier of the signer's certificate. This member can optionally be used with PKCS #7 with Cryptographic Message Syntax (CMS). If this member is not <b>NULL</b> and its <b>dwIdChoice</b> member is not zero, it is used to identify  the certificate instead of the <b>Issuer</b> and <b>SerialNumber</b> members of the <a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a> structure pointed to by <b>pCertInfo</b>.
						CMS supports the KEY_IDENTIFIER and ISSUER_SERIAL_NUMBER CERT_ID structures. PKCS version 1.5 supports only the ISSUER_SERIAL_NUMBER CERT_ID choice. This member is  used with CMS for PKCS #7 processing and can be used only if CMSG_SIGNER_ENCODE_INFO_HAS_CMS_FIELDS is defined.


### -field HashEncryptionAlgorithm

A 
						<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure optionally used with PKCS #7 with CMS. If this member is not <b>NULL</b>, the algorithm identified is used instead of the SubjectPublicKeyInfo.Algorithm algorithm.
If this member is set to szOID_PKIX_NO_SIGNATURE, the signature value contains only the hash octets. 

For RSA, the <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> encryption algorithm is normally the same as the public key algorithm. For DSA, the hash encryption algorithm is normally a DSS signature algorithm.

This member is  used with CMS for PKCS #7 processing and can be used only if CMSG_SIGNER_ENCODE_INFO_HAS_CMS_FIELDS is defined.


### -field pvHashEncryptionAuxInfo

This member is not used. This member must be set to <b>NULL</b> if it is present in the data structure.
This member is present only if CMSG_SIGNER_ENCODE_INFO_HAS_CMS_FIELDS is defined.


## -see-also




<a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a>



<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="https://msdn.microsoft.com/cdbaf38d-ddbe-4be0-afbc-f8bd76ef4847">CRYPT_ATTRIBUTE</a>



<a href="https://msdn.microsoft.com/a990d44d-2993-429f-b817-2a834105ecef">CryptMsgControl</a>



<a href="https://msdn.microsoft.com/ebf76664-bca6-462d-b519-2b60f435d8ef">CryptMsgCountersign</a>
 

 

