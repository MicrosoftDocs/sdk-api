---
UID: NF:certenroll.IX509AttributeArchiveKey.InitializeEncode
title: IX509AttributeArchiveKey::InitializeEncode method
author: windows-driver-content
description: Initializes the attribute from an IX509PrivateKey object, the certification authority encryption certificate, and the symmetric encryption algorithm object identifier (OID).
old-location: security\ix509attributearchivekey_initializeencode_method.htm
old-project: SecCertEnroll
ms.assetid: 44865c22-0eca-4781-962c-a10698a435f4
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: IX509AttributeArchiveKey, IX509AttributeArchiveKey interface [Security], InitializeEncode method, IX509AttributeArchiveKey::InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security], IX509AttributeArchiveKey interface, InitializeEncode,IX509AttributeArchiveKey.InitializeEncode, certenroll/IX509AttributeArchiveKey::InitializeEncode, security.ix509attributearchivekey_initializeencode_method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509AttributeArchiveKey.InitializeEncode
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509AttributeArchiveKey::InitializeEncode method


## -description


The <b>InitializeEncode</b> method initializes the attribute from an <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> object, the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> encryption certificate, and the symmetric encryption algorithm <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID).


## -parameters




### -param pKey [in]

Pointer to an <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> interface that represents the key.


### -param Encoding [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to the input string that contains the encrypted key.


### -param strCAXCert [in]

A <b>BSTR</b> variable that contains the certification authority encryption certificate that contains the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> used to encrypt the private key.

Beginning with Windows 7 and Windows Server 2008 R2, you can specify a certificate thumb print or serial number rather than an encoded certificate. Doing so causes the function to search the appropriate local stores for the matching certificate. Keep in mind the following points:

<ul>
<li>The <b>BSTR</b> must be an even number of hexadecimal digits.</li>
<li>Whitespace between hexadecimal pairs is ignored.</li>
<li>The <i>Encoding</i> parameter must be set to <b>XCN_CRYPT_STRING_HEXRAW</b>.</li>
<li>Only the personal and request stores are searched for the private key.</li>
</ul>

### -param pAlgorithm [in, optional]

Pointer to an <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> interface that represents the OID of the symmetric encryption algorithm used to encrypt the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a>. This parameter is optional. If you do not supply an OID, XCN_OID_RSA_DES_EDE3_CBC (Triple DES) is used.


### -param EncryptionStrength [in]

A <b>LONG</b> variable that contains the encryption strength of the algorithm identified by the <i>pAlgorithm</i> parameter. This parameter is not currently used because the Certificate Enrollment SDK does not support any algorithms for which the OID does not already imply the strength (key length). For example, AES has multiple strengths but strength each is already indicated by the OID.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The object identifier for this attribute is <b>XCN_OID_ARCHIVED_KEY_ATTR</b> (1.3.6.1.4.1.311.21.13). For more information, see <a href="https://msdn.microsoft.com/30e8c740-854b-409f-a138-3871df305708">CERTENROLL_OBJECTID</a>.

You must call either <b>InitializeEncode</b> or <a href="https://msdn.microsoft.com/d6c39eaa-53d1-4cc4-bed3-34c9ef62e9d0">InitializeDecode</a> before you can use an <a href="https://msdn.microsoft.com/b42111e9-e39e-4192-9aba-47403fb627dc">IX509AttributeArchiveKey</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct an encoded <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) structure from raw data, and the <b>InitializeDecode</b> method enables you to initialize raw data from an encoded ASN.1 structure. You can call the following properties to retrieve the raw data:<ul>
<li>
<a href="https://msdn.microsoft.com/7aef6c1e-c3f1-4124-b397-bf13ca610135">EncryptionAlgorithm</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3230cfbf-5486-4f77-9efe-5bc542e3e096">EncryptedKeyBlob</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c365a2e0-caff-4c92-aa22-33c165ea672e">EncryptionStrength</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/b42111e9-e39e-4192-9aba-47403fb627dc">IX509AttributeArchiveKey</a>
 

 

