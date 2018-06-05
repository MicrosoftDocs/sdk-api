---
UID: NF:certenroll.IX509AttributeArchiveKey.get_EncryptionAlgorithm
title: IX509AttributeArchiveKey::get_EncryptionAlgorithm
author: windows-sdk-content
description: Retrieves the object identifier (OID) of the symmetric encryption algorithm used to encrypt the private key.
old-location: security\ix509attributearchivekey_encryptionalgorithm_property.htm
old-project: SecCertEnroll
ms.assetid: 7aef6c1e-c3f1-4124-b397-bf13ca610135
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: EncryptionAlgorithm property [Security], EncryptionAlgorithm property [Security],IX509AttributeArchiveKey interface, IX509AttributeArchiveKey interface [Security],EncryptionAlgorithm property, IX509AttributeArchiveKey.EncryptionAlgorithm, IX509AttributeArchiveKey.get_EncryptionAlgorithm, IX509AttributeArchiveKey::EncryptionAlgorithm, IX509AttributeArchiveKey::get_EncryptionAlgorithm, certenroll/IX509AttributeArchiveKey::EncryptionAlgorithm, certenroll/IX509AttributeArchiveKey::get_EncryptionAlgorithm, get_EncryptionAlgorithm, security.ix509attributearchivekey_encryptionalgorithm_property
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509AttributeArchiveKey.EncryptionAlgorithm
-	IX509AttributeArchiveKey.get_EncryptionAlgorithm
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509AttributeArchiveKey::get_EncryptionAlgorithm


## -description


The <b>EncryptionAlgorithm</b> property retrieves the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) of the symmetric encryption algorithm used to encrypt the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a>.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/44865c22-0eca-4781-962c-a10698a435f4">InitializeEncode</a> method or the  <a href="https://msdn.microsoft.com/d6c39eaa-53d1-4cc4-bed3-34c9ef62e9d0">InitializeDecode</a> method to initialize the <b>EncryptionAlgorithm</b> property. You can call the following properties to retrieve the raw data:

<ul>
<li>
<a href="https://msdn.microsoft.com/3230cfbf-5486-4f77-9efe-5bc542e3e096">EncryptedKeyBlob</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c365a2e0-caff-4c92-aa22-33c165ea672e">EncryptionStrength</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/b42111e9-e39e-4192-9aba-47403fb627dc">IX509AttributeArchiveKey</a>
 

 

