---
UID: NS:wincrypt._CMSG_ENVELOPED_ENCODE_INFO
title: "_CMSG_ENVELOPED_ENCODE_INFO"
author: windows-sdk-content
description: Contains information needed to encode an enveloped message. It is passed to CryptMsgOpenToEncode if the dwMsgType parameter is CMSG_ENVELOPED.
old-location: security\cmsg_enveloped_encode_info.htm
old-project: SecCrypto
ms.assetid: 87712541-2806-4709-a7cf-c9ba966c96fd
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: "*PCMSG_ENVELOPED_ENCODE_INFO, All other encryption algorithms, CALG_3DES, CALG_DES, CMSG_ENVELOPED_ENCODE_INFO, CMSG_ENVELOPED_ENCODE_INFO structure [Security], PCMSG_ENVELOPED_ENCODE_INFO, PCMSG_ENVELOPED_ENCODE_INFO structure pointer [Security], RC2, RC4, SP3 or compatible, _CMSG_ENVELOPED_ENCODE_INFO, _crypto2_cmsg_enveloped_encode_info, security.cmsg_enveloped_encode_info, wincrypt/CMSG_ENVELOPED_ENCODE_INFO, wincrypt/PCMSG_ENVELOPED_ENCODE_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.redist: 
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
req.typenames: CMSG_ENVELOPED_ENCODE_INFO, *PCMSG_ENVELOPED_ENCODE_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CMSG_ENVELOPED_ENCODE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CMSG_ENVELOPED_ENCODE_INFO structure


## -description


The <b>CMSG_ENVELOPED_ENCODE_INFO</b> structure contains information needed to encode an enveloped message. It is passed to 
<a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a> if the <i>dwMsgType</i> parameter is CMSG_ENVELOPED.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field hCryptProv

This member is not used and should be set to <b>NULL</b>.

<b>Windows Server 2003 and Windows XP:  </b>Specifies a handle to the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) used to do content encryption, recipient key encryption, and export. The private keys of the <b>hCryptProv</b> are not used. 


This member's data type is <b>HCRYPTPROV</b>.

Unless there is a strong reason for passing in a specific cryptographic provider in <b>hCryptProv</b>, pass zero to use the default RSA or DSS provider.




### -field ContentEncryptionAlgorithm

A <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the signature algorithm type and any associated additional parameters in encoded form. 




The <b>pszObjId</b> member of the structure specifies the algorithm used to encrypt the message contents.

The following encryption algorithms require an encoded eight byte <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">initialization vector</a> (IV) in the <b>Parameters</b> member of structure. For details, see 
<a href="https://msdn.microsoft.com/e99a84a2-c23e-4251-8062-dd286ccc29b7">CryptSetKeyParam</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CALG_DES"></a><a id="calg_des"></a><dl>
<dt><b>CALG_DES</b></dt>
</dl>
</td>
<td width="60%">
szOID_OIWSEC_desCBC

</td>
</tr>
<tr>
<td width="40%"><a id="CALG_3DES"></a><a id="calg_3des"></a><dl>
<dt><b>CALG_3DES</b></dt>
</dl>
</td>
<td width="60%">
szOID_RSA_DES_EDE3_CBC

</td>
</tr>
</table>
 

If the <b>cbData</b> member of the <b>Parameters</b> member is zero, an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoded OCTET STRING containing the IV is generated using 
<a href="https://msdn.microsoft.com/3e5a437f-7439-43c9-a191-2908d2df0eb6">CryptGenRandom</a>.

The szOID_RSA_RC2CBC (CALG_RC2) algorithm requires the <b>pbData</b> member of <b>Parameters</b> to be an encoded 
<a href="https://msdn.microsoft.com/58b1dc44-55ea-4c22-a115-dfeaee8a2297">CRYPT_RC2_CBC_PARAMETERS</a> structure. If the <b>cbData</b> member of the <b>Parameters</b> member is zero, an ASN.1 encoded CRYPT_RC2_CBC_PARAMETERS is generated with a default value of 40 for the <b>dwVersion</b> member. This sets the default key length to 40 bits. This default key length can be overridden with <b>pvEncryptionAuxInfo</b> pointing to a 
<a href="https://msdn.microsoft.com/6d7014fa-2d0c-48de-bda5-91d19ad879f9">CMSG_RC2_AUX_INFO</a> structure containing the desired key length.

<div class="alert"><b>Note</b>  On decryption, if an IV exists, 
<a href="https://msdn.microsoft.com/e99a84a2-c23e-4251-8062-dd286ccc29b7">CryptSetKeyParam</a> is called with the IV before decryption begins.</div>
<div> </div>

### -field pvEncryptionAuxInfo

A pointer to a structure depending on the encryption algorithm. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RC2"></a><a id="rc2"></a><dl>
<dt><b>RC2</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/6d7014fa-2d0c-48de-bda5-91d19ad879f9">CMSG_RC2_AUX_INFO</a>


</td>
</tr>
<tr>
<td width="40%"><a id="RC4"></a><a id="rc4"></a><dl>
<dt><b>RC4</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/8e456156-b84a-4ca7-9dc7-9f5da4a32a6c">CMSG_RC4_AUX_INFO</a>


</td>
</tr>
<tr>
<td width="40%"><a id="SP3_or_compatible"></a><a id="sp3_or_compatible"></a><a id="SP3_OR_COMPATIBLE"></a><dl>
<dt><b>SP3 or compatible</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/9afd38c5-fccd-43ea-9c30-c62fdcbee633">CMSG_SP3_COMPATIBLE_AUX_INFO</a>


</td>
</tr>
<tr>
<td width="40%"><a id="All_other_encryption_algorithms"></a><a id="all_other_encryption_algorithms"></a><a id="ALL_OTHER_ENCRYPTION_ALGORITHMS"></a><dl>
<dt><b>All other encryption algorithms</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b>

</td>
</tr>
</table>
 


### -field cRecipients

Number of elements in the <b>rgpRecipients</b> or <b>rgCmsRecipients</b> array.


### -field rgpRecipients

An array of pointers to 
<a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a> structures, each containing a recipient's certificate Issuer, SerialNumber, and SubjectPublicKeyInfo. This array can only be used for recipients identified by their Issuer and serial number. If <b>rgpRecipients</b> is not <b>NULL</b>, <b>rgCmsRecipients</b> must be <b>NULL</b>.


### -field rgCmsRecipients

Optional. An array of pointers to <a href="https://msdn.microsoft.com/eb85f3e4-a5f8-45e7-9bbf-9c649db1e141">CMSG_RECIPIENT_ENCODE_INFO</a> structures containing recipient information. If <b>rgCmsRecipients</b> is not <b>NULL</b>, <b>rgpRecipients</b> must be <b>NULL</b>. CMSG_ENVELOPED_ENCODE_INFO_HAS_CMS_FIELDS must be defined to reference this field.


### -field cCertEncoded

Optional. A <b>DWORD</b> value that indicates the number of encoded certificates in the <b>rgCertEncoded</b> array. CMSG_ENVELOPED_ENCODE_INFO_HAS_CMS_FIELDS must be defined to reference this field.


### -field rgCertEncoded

Optional. Array of <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CERT_BLOB</a> structures. CMSG_ENVELOPED_ENCODE_INFO_HAS_CMS_FIELDS must be defined to reference this field.


### -field cCrlEncoded

Optional. A <b>DWORD</b> value that indicates the number of encoded <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation lists</a> (CRLs) in the <b>rgCRLEncoded</b> array. CMSG_ENVELOPED_ENCODE_INFO_HAS_CMS_FIELDS must be defined to reference this field.


### -field rgCrlEncoded

Optional. An array of <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRL_BLOB</a> structures. CMSG_ENVELOPED_ENCODE_INFO_HAS_CMS_FIELDS must be defined to reference this field.


### -field cAttrCertEncoded

Optional. A <b>DWORD</b> value that indicates the number of encoded certificate attributes in the <b>rgAttrCertEncoded</b> array. CMSG_ENVELOPED_ENCODE_INFO_HAS_CMS_FIELDS must be defined to reference this field.


### -field rgAttrCertEncoded

Optional. An array of <a href="https://msdn.microsoft.com/cdbaf38d-ddbe-4be0-afbc-f8bd76ef4847">CRYPT_ATTRIBUTE</a> structures. CMSG_ENVELOPED_ENCODE_INFO_HAS_CMS_FIELDS must be defined to reference this member.


### -field cUnprotectedAttr

Optional. A <b>DWORD</b> value that indicates the number of unprotected attributes in the <b>rgUnprotectedAttr</b> array. CMSG_ENVELOPED_ENCODE_INFO_HAS_CMS_FIELDS must be defined to reference this field.


### -field rgUnprotectedAttr

Optional. An array of <a href="https://msdn.microsoft.com/cdbaf38d-ddbe-4be0-afbc-f8bd76ef4847">CRYPT_ATTRIBUTE</a> structures. CMSG_ENVELOPED_ENCODE_INFO_HAS_CMS_FIELDS must be defined to reference this field.


## -see-also




<a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a>



<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a>
 

 

