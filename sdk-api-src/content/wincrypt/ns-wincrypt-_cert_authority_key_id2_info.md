---
UID: NS:wincrypt._CERT_AUTHORITY_KEY_ID2_INFO
title: "_CERT_AUTHORITY_KEY_ID2_INFO"
author: windows-sdk-content
description: The CERT_AUTHORITY_KEY_ID2_INFO structure identifies the key used to sign a certificate or CRL.
old-location: security\cert_authority_key_id2_info.htm
tech.root: seccrypto
ms.assetid: 0a5005a5-71be-4f4d-8de8-c7452402b646
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: "*PCERT_AUTHORITY_KEY_ID2_INFO, CERT_AUTHORITY_KEY_ID2_INFO, CERT_AUTHORITY_KEY_ID2_INFO structure [Security], PCERT_AUTHORITY_KEY_ID2_INFO, PCERT_AUTHORITY_KEY_ID2_INFO structure pointer [Security], _CERT_AUTHORITY_KEY_ID2_INFO, _crypto2_cert_authority_key_id2_info, security.cert_authority_key_id2_info, wincrypt/CERT_AUTHORITY_KEY_ID2_INFO, wincrypt/PCERT_AUTHORITY_KEY_ID2_INFO"
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
 - CERT_AUTHORITY_KEY_ID2_INFO
product: Windows
targetos: Windows
req.typenames: CERT_AUTHORITY_KEY_ID2_INFO, *PCERT_AUTHORITY_KEY_ID2_INFO
req.redist: 
---

# _CERT_AUTHORITY_KEY_ID2_INFO structure


## -description


The <b>CERT_AUTHORITY_KEY_ID2_INFO</b> structure identifies the key used to sign a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate</a> or <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">CRL</a>. It differs from the 
<a href="https://msdn.microsoft.com/2f966d39-8d7c-41e7-bf6a-5a30170b100d">CERT_AUTHORITY_KEY_ID_INFO</a> structure in that the certificate issuer is a 
<a href="https://msdn.microsoft.com/f9a20827-3333-4ce2-b074-2e8ce903fad2">CERT_ALT_NAME_INFO</a> instead of a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CERT_NAME_BLOB</a>. Otherwise, the structures are used in the same way.

The key can be identified by an explicit key identifier, by giving a certificate's issuer and serial number, or by both. If both are used, the certificate issuer must ensure that the explicit key identifier, the certificate issuer and the serial number are consistent.


<a href="https://msdn.microsoft.com/7d5ed4f4-9d76-4a16-9059-27b0edd83459">CryptDecodeObject</a> creates an instance of this structure when performed on a 
<a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a> structure's <b>Value</b> member with its the structure's <b>pszObjId</b> member set to szOID_AUTHORITY_KEY_IDENTIFIER2.

An instance of this structure can be used as input to <a href="https://msdn.microsoft.com/9576a2a7-4379-4c1b-8ad5-284720cf7ccc">CryptEncodeObject</a> to create an appropriate <a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a>.
		


## -struct-fields




### -field KeyId

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that contains a unique identifier of a public key.


### -field AuthorityCertIssuer


<a href="https://msdn.microsoft.com/f9a20827-3333-4ce2-b074-2e8ce903fad2">CERT_ALT_NAME_INFO</a> that includes the encoded name of the CA that issued the certificate. The <b>cAltEntry</b> member of the structure may be set to zero if the name is not to be used to identify the CA.


### -field AuthorityCertSerialNumber

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a> structure that includes the serial number of the certificate associated with the private key used to sign this certificate. For more information, see 
<a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a>.


## -see-also




<a href="https://msdn.microsoft.com/f9a20827-3333-4ce2-b074-2e8ce903fad2">CERT_ALT_NAME_INFO</a>



<a href="https://msdn.microsoft.com/2f966d39-8d7c-41e7-bf6a-5a30170b100d">CERT_AUTHORITY_KEY_ID_INFO</a>
 

 

