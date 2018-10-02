---
UID: NS:dpapi._CRYPTOAPI_BLOB
title: "_CRYPTOAPI_BLOB"
author: windows-sdk-content
description: The CryptoAPI CRYPT_INTEGER_BLOB structure is used for an arbitrary array of bytes. It is declared in Wincrypt.h and provides flexibility for objects that can contain various data types.
old-location: security\cryptoapi_blob.htm
tech.root: seccrypto
ms.assetid: 1c2a07b8-f702-47f3-8d4c-6ac0cbc63f0f
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: "*PCERT_BLOB, *PCERT_NAME_BLOB, *PCERT_RDN_VALUE_BLOB, *PCRL_BLOB, *PCRYPT_ATTR_BLOB, *PCRYPT_DATA_BLOB, *PCRYPT_DER_BLOB, *PCRYPT_DIGEST_BLOB, *PCRYPT_HASH_BLOB, *PCRYPT_INTEGER_BLOB, *PCRYPT_OBJID_BLOB, *PCRYPT_UINT_BLOB, *PDATA_BLOB, CERT_BLOB, CERT_BLOB structure [Security], CERT_NAME_BLOB, CERT_NAME_BLOB structure [Security], CERT_RDN_VALUE_BLOB, CERT_RDN_VALUE_BLOB structure [Security], CRL_BLOB, CRL_BLOB structure [Security], CRYPTOAPI_BLOB, CRYPTOAPI_BLOB structure [Security], CRYPT_ATTR_BLOB, CRYPT_ATTR_BLOB structure [Security], CRYPT_DATA_BLOB, CRYPT_DATA_BLOB structure [Security], CRYPT_DER_BLOB, CRYPT_DER_BLOB structure [Security], CRYPT_DIGEST_BLOB, CRYPT_DIGEST_BLOB structure [Security], CRYPT_HASH_BLOB, CRYPT_HASH_BLOB structure [Security], CRYPT_INTEGER_BLOB, CRYPT_INTEGER_BLOB structure [Security], CRYPT_OBJID_BLOB, CRYPT_OBJID_BLOB structure [Security], CRYPT_UINT_BLOB, CRYPT_UINT_BLOB structure [Security], DATA_BLOB, DATA_BLOB structure [Security], PCERT_BLOB, PCERT_BLOB structure pointer [Security], PCERT_NAME_BLOB, PCERT_NAME_BLOB structure pointer [Security], PCERT_RDN_VALUE_BLOB, PCERT_RDN_VALUE_BLOB structure pointer [Security], PCRL_BLOB, PCRL_BLOB structure pointer [Security], PCRYPT_ATTR_BLOB, PCRYPT_ATTR_BLOB structure pointer [Security], PCRYPT_DATA_BLOB, PCRYPT_DATA_BLOB structure pointer [Security], PCRYPT_DER_BLOB, PCRYPT_DER_BLOB structure pointer [Security], PCRYPT_DIGEST_BLOB, PCRYPT_DIGEST_BLOB structure pointer [Security], PCRYPT_HASH_BLOB, PCRYPT_HASH_BLOB structure pointer [Security], PCRYPT_INTEGER_BLOB, PCRYPT_INTEGER_BLOB structure pointer [Security], PCRYPT_OBJID_BLOB, PCRYPT_OBJID_BLOB structure pointer [Security], PCRYPT_UINT_BLOB, PCRYPT_UINT_BLOB structure pointer [Security], PDATA_BLOB, PDATA_BLOB structure pointer [Security], _CRYPTOAPI_BLOB, _crypto2_cryptoapi_blob, dpapi/CERT_BLOB, dpapi/CERT_NAME_BLOB, dpapi/CERT_RDN_VALUE_BLOB, dpapi/CRL_BLOB, dpapi/CRYPTOAPI_BLOB, dpapi/CRYPT_ATTR_BLOB, dpapi/CRYPT_DATA_BLOB, dpapi/CRYPT_DER_BLOB, dpapi/CRYPT_DIGEST_BLOB, dpapi/CRYPT_HASH_BLOB, dpapi/CRYPT_OBJID_BLOB, dpapi/CRYPT_UINT_BLOB, dpapi/DATA_BLOB, dpapi/PCERT_BLOB, dpapi/PCERT_NAME_BLOB, dpapi/PCERT_RDN_VALUE_BLOB, dpapi/PCRL_BLOB, dpapi/PCRYPT_ATTR_BLOB, dpapi/PCRYPT_DATA_BLOB, dpapi/PCRYPT_DER_BLOB, dpapi/PCRYPT_DIGEST_BLOB, dpapi/PCRYPT_HASH_BLOB, dpapi/PCRYPT_INTEGER_BLOB, dpapi/PCRYPT_OBJID_BLOB, dpapi/PCRYPT_UINT_BLOB, dpapi/PDATA_BLOB, security.cryptoapi_blob"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dpapi.h
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
 - dpapi.h
api_name:
 - CRYPT_INTEGER_BLOB
product: Windows
targetos: Windows
req.typenames: CRYPT_INTEGER_BLOB, *PCRYPT_INTEGER_BLOB, CRYPT_UINT_BLOB, *PCRYPT_UINT_BLOB, CRYPT_OBJID_BLOB, *PCRYPT_OBJID_BLOB, CERT_NAME_BLOB, *PCERT_NAME_BLOB, CERT_RDN_VALUE_BLOB, *PCERT_RDN_VALUE_BLOB, CERT_BLOB, *PCERT_BLOB, CRL_BLOB, *PCRL_BLOB, DATA_BLOB, *PDATA_BLOB, CRYPT_DATA_BLOB, *PCRYPT_DATA_BLOB, CRYPT_HASH_BLOB, *PCRYPT_HASH_BLOB, CRYPT_DIGEST_BLOB, *PCRYPT_DIGEST_BLOB, CRYPT_DER_BLOB, *PCRYPT_DER_BLOB, CRYPT_ATTR_BLOB, *PCRYPT_ATTR_BLOB
req.redist: 
---

# _CRYPTOAPI_BLOB structure


## -description


The CryptoAPI <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a> structure is used for an arbitrary array of bytes. It is declared in Wincrypt.h and provides flexibility for objects that can contain various data types.


## -struct-fields




### -field cbData

The count of bytes in the buffer pointed to by <i>pbData</i>.
					


### -field pbData

A pointer to a block of data bytes.


## -see-also




<a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a>



<a href="https://msdn.microsoft.com/86b1716d-541f-4e06-a824-01c22f0eba27">CERT_POLICY_QUALIFIER_INFO</a>



<a href="https://msdn.microsoft.com/6edeed33-16e1-4295-90e9-769929ab916a">CERT_REQUEST_INFO</a>



<a href="https://msdn.microsoft.com/5e347a50-942e-4278-a9ae-ad4c30c55c6b">CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA</a>



<a href="https://msdn.microsoft.com/eae631d2-5e5f-4964-b079-9692831b34fc">CMSG_SIGNER_INFO</a>



<a href="https://msdn.microsoft.com/84057581-d0a9-464a-9399-ba806e37516f">CRYPT_ATTRIBUTE_TYPE_VALUE</a>



<a href="https://msdn.microsoft.com/876527dd-1ec5-4783-a7ad-20a0e2d2367a">CRYPT_TIME_STAMP_REQUEST_INFO</a>



<a href="https://msdn.microsoft.com/467ce464-2f22-4583-a745-711ba3b05f4f">CertCompareIntegerBlob</a>



<a href="https://msdn.microsoft.com/b3d96de8-5cbc-4ccb-b759-6757520bbda3">CertNameToStr</a>
 

 

