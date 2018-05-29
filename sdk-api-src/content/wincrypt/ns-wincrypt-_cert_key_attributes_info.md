---
UID: NS:wincrypt._CERT_KEY_ATTRIBUTES_INFO
title: "_CERT_KEY_ATTRIBUTES_INFO"
author: windows-sdk-content
description: The CERT_KEY_ATTRIBUTES_INFO structure contains optional additional information about the public key being certified.
old-location: security\cert_key_attributes_info.htm
old-project: SecCrypto
ms.assetid: cedf0321-4f5a-48a9-abfd-d8642bb89576
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: "*PCERT_KEY_ATTRIBUTES_INFO, CERT_KEY_ATTRIBUTES_INFO, CERT_KEY_ATTRIBUTES_INFO structure [Security], PCERT_KEY_ATTRIBUTES_INFO, PCERT_KEY_ATTRIBUTES_INFO structure pointer [Security], _CERT_KEY_ATTRIBUTES_INFO, _crypto2_cert_key_attributes_info, security.cert_key_attributes_info, wincrypt/CERT_KEY_ATTRIBUTES_INFO, wincrypt/PCERT_KEY_ATTRIBUTES_INFO"
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
req.typenames: CERT_KEY_ATTRIBUTES_INFO, *PCERT_KEY_ATTRIBUTES_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CERT_KEY_ATTRIBUTES_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CERT_KEY_ATTRIBUTES_INFO structure


## -description


The <b>CERT_KEY_ATTRIBUTES_INFO</b> structure contains optional additional information about the public key being certified. It can include a key identifier, an indication of the intended use of that key, or an indication of the period of use of the corresponding private key.


<a href="https://msdn.microsoft.com/7d5ed4f4-9d76-4a16-9059-27b0edd83459">CryptDecodeObject</a> creates an instance of this structure when performed on a 
<a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a> structure's <b>Value</b> member with its the structure's <b>pszObjId</b> member set to szOID_KEY_ATTRIBUTES.

An instance of this structure can be used as input to <a href="https://msdn.microsoft.com/9576a2a7-4379-4c1b-8ad5-284720cf7ccc">CryptEncodeObject</a> to create an appropriate <a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a>.


## -struct-fields




### -field KeyId

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure with a unique identifier of a key.


### -field IntendedKeyUsage

<b>CRYPT_BIT_BLOB</b> with it <b>pbData</b> member indicating the intended purpose of the key. For a list of usage bit values, see the <b>RestrictedKeyUsage</b> member of 
the <a href="https://msdn.microsoft.com/f949c8e5-055d-4919-abcc-441880ccce56">CERT_KEY_USAGE_RESTRICTION_INFO</a> structure. 




This member can be used to find the correct key or certificate of a user who has multiple keys or certificates. Its indication of usage is advisory field, only, and does not imply that usage of the key is restricted to the purpose indicated. The list of intended uses is not necessarily all-inclusive, and the field can be omitted. If a key is to be restricted to a particular use a <a href="https://msdn.microsoft.com/f949c8e5-055d-4919-abcc-441880ccce56">CERT_KEY_USAGE_RESTRICTION_INFO</a> extension must be used.


### -field pPrivateKeyUsagePeriod

A pointer to a 
<a href="https://msdn.microsoft.com/4764174f-eecc-402e-8395-d3e2be0b0ae6">CERT_PRIVATE_KEY_VALIDITY</a> structure that indicates the period of use of the private key corresponding to the certified public key. This member is optional and can be set to <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a>



<a href="https://msdn.microsoft.com/4764174f-eecc-402e-8395-d3e2be0b0ae6">CERT_PRIVATE_KEY_VALIDITY</a>



<a href="https://msdn.microsoft.com/6f102ff3-bfff-4415-a5d8-ca2c226074b3">CRYPT_BIT_BLOB</a>



<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>



<a href="https://msdn.microsoft.com/7d5ed4f4-9d76-4a16-9059-27b0edd83459">CryptDecodeObject</a>
 

 

