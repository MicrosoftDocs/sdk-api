---
UID: NS:wincrypt._CERT_AUTHORITY_KEY_ID_INFO
title: "_CERT_AUTHORITY_KEY_ID_INFO"
author: windows-driver-content
description: Identifies the key used to sign a certificate or certificate revocation list (CRL).
old-location: security\cert_authority_key_id_info.htm
old-project: SecCrypto
ms.assetid: 2f966d39-8d7c-41e7-bf6a-5a30170b100d
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: "*PCERT_AUTHORITY_KEY_ID_INFO, CERT_AUTHORITY_KEY_ID_INFO, CERT_AUTHORITY_KEY_ID_INFO structure [Security], PCERT_AUTHORITY_KEY_ID_INFO, PCERT_AUTHORITY_KEY_ID_INFO structure pointer [Security], _CERT_AUTHORITY_KEY_ID_INFO, _crypto2_cert_authority_key_id_info, security.cert_authority_key_id_info, wincrypt/CERT_AUTHORITY_KEY_ID_INFO, wincrypt/PCERT_AUTHORITY_KEY_ID_INFO"
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
req.typenames: CERT_AUTHORITY_KEY_ID_INFO, *PCERT_AUTHORITY_KEY_ID_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CERT_AUTHORITY_KEY_ID_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CERT_AUTHORITY_KEY_ID_INFO structure


## -description


The <b>CERT_AUTHORITY_KEY_ID_INFO</b> structure identifies the key used to sign a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate</a> or <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL). This structure differentiates among distinct keys used by the same <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> as, for example, keys changed when an update occurs.

The key can be identified by an explicit key identifier, by giving a certificate's issuer and serial number, or by both. If both are used, the certificate issuer must ensure that the explicit key identifier, the certificate issuer and the serial number are consistent.


<a href="https://msdn.microsoft.com/7d5ed4f4-9d76-4a16-9059-27b0edd83459">CryptDecodeObject</a> creates an instance of this structure when performed on a 
<a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a> structure's <b>Value</b> member with its structure's <b>pszObjId</b> member set to szOID_AUTHORITY_KEY_IDENTIFIER.

An instance of this structure can be used as input to <a href="https://msdn.microsoft.com/9576a2a7-4379-4c1b-8ad5-284720cf7ccc">CryptEncodeObject</a> to create an appropriate <a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a>.


## -struct-fields




### -field KeyId

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that contains a unique identifier of a public key.


### -field CertIssuer

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CERT_NAME_BLOB</a> structure that contains the encoded distinguished name of the certification authority that issued the certificate.


### -field CertSerialNumber

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a> structure that contains the serial number of the certificate associated with the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> used to sign this certificate. For more information, see 
<a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a>.


## -see-also




<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>
 

 

