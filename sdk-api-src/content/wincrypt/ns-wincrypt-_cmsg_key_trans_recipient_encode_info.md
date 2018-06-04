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

# _CMSG_KEY_TRANS_RECIPIENT_ENCODE_INFO structure


## -description


The <b>CMSG_KEY_TRANS_RECIPIENT_ENCODE_INFO</b> structure contains encoded key transport information for a message recipient.


## -struct-fields




### -field cbSize

A <b>DWORD</b> value that indicates the size, in bytes, of the structure.


### -field KeyEncryptionAlgorithm

A 
						<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> value that identifies the key-encryption algorithm and any associated parameters used to encrypt the content encryption key.

For RSA AES,  the <b>pszObjId</b> member of the <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure  should be set to szOID_RSAES_OAEP. The <b>Parameters</b> member of the  <b>CRYPT_ALGORITHM_IDENTIFIER</b> structure should be set to the encoded <b>PKCS_RSAES_OAEP_PARAMETERS</b>. If the <b>Parameters.cbData</b> member is equal to zero, then the default parameters are used and encoded.


### -field pvKeyEncryptionAuxInfo

A void pointer to a structure that contains additional information about the encryption. The format of the structure is dependent upon the algorithm indicated by <b>KeyEncryptionAlgorithm</b>.


### -field hCryptProv

This member is not used and should be set to <b>NULL</b>.

<b>Windows Server 2003 and Windows XP:  </b> A <a href="https://msdn.microsoft.com/8ec6b392-06bc-4717-8657-7ea9a43d03fb">HCRYPTPROV</a> value used to do the recipient key encryption and export. The provider's private keys are not used. If <b>hCryptProv</b> is <b>NULL</b>, the <b>HCRYPTPROV</b> specified in the 
<a href="https://msdn.microsoft.com/87712541-2806-4709-a7cf-c9ba966c96fd">CMSG_ENVELOPED_ENCODE_INFO</a> is used.Note that this <a href="https://msdn.microsoft.com/8ec6b392-06bc-4717-8657-7ea9a43d03fb">HCRYPTPROV</a> is not released even if CMSG_CRYPT_RELEASE_CONTEXT_FLAG is set in the <i>dwFlags</i> parameter passed to <a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a>.




### -field RecipientPublicKey

A <b>CRYPT_BIT_BLOB</b> variable that contains the public key of the recipient.


### -field RecipientId


						A <a href="https://msdn.microsoft.com/9e33f661-c365-4725-8c3f-27b6cdd9a84e">CERT_ID</a> value that identifies the recipient. CMS supports the KEY_IDENTIFIER and ISSUER_SERIAL_NUMBER <b>CERT_ID</b>s. PKCS #7 version 1.5 supports only the ISSUER_SERIAL_NUMBER <b>CERT_ID</b>s.

