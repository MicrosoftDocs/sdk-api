---
UID: NF:certenroll.IX509AttributeArchiveKey.get_EncryptedKeyBlob
title: IX509AttributeArchiveKey::get_EncryptedKeyBlob
author: windows-sdk-content
description: Retrieves a byte array that contains the encrypted key.
old-location: security\ix509attributearchivekey_encryptedkeyblob_property.htm
tech.root: SecCertEnroll
ms.assetid: 3230cfbf-5486-4f77-9efe-5bc542e3e096
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EncryptedKeyBlob property [Security], EncryptedKeyBlob property [Security],IX509AttributeArchiveKey interface, IX509AttributeArchiveKey interface [Security],EncryptedKeyBlob property, IX509AttributeArchiveKey.EncryptedKeyBlob, IX509AttributeArchiveKey.get_EncryptedKeyBlob, IX509AttributeArchiveKey::EncryptedKeyBlob, IX509AttributeArchiveKey::get_EncryptedKeyBlob, certenroll/IX509AttributeArchiveKey::EncryptedKeyBlob, certenroll/IX509AttributeArchiveKey::get_EncryptedKeyBlob, get_EncryptedKeyBlob, security.ix509attributearchivekey_encryptedkeyblob_property
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
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509AttributeArchiveKey.EncryptedKeyBlob
 - IX509AttributeArchiveKey.get_EncryptedKeyBlob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509AttributeArchiveKey::get_EncryptedKeyBlob


## -description


The <b>EncryptedKeyBlob</b> property retrieves a byte array that contains the encrypted key. The byte array is represented by a Unicode-encoded string.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/44865c22-0eca-4781-962c-a10698a435f4">InitializeEncode</a> method or the  <a href="https://msdn.microsoft.com/d6c39eaa-53d1-4cc4-bed3-34c9ef62e9d0">InitializeDecode</a> method to initialize the <b>EncryptedKeyBlob</b> property. You can call the following properties to retrieve the raw data:

<ul>
<li>
<a href="https://msdn.microsoft.com/7aef6c1e-c3f1-4124-b397-bf13ca610135">EncryptionAlgorithm</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c365a2e0-caff-4c92-aa22-33c165ea672e">EncryptionStrength</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/b42111e9-e39e-4192-9aba-47403fb627dc">IX509AttributeArchiveKey</a>
 

 

