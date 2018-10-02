---
UID: NF:certenroll.IX509AttributeArchiveKey.get_EncryptionAlgorithm
title: IX509AttributeArchiveKey::get_EncryptionAlgorithm
author: windows-sdk-content
description: Retrieves the object identifier (OID) of the symmetric encryption algorithm used to encrypt the private key.
old-location: security\ix509attributearchivekey_encryptionalgorithm_property.htm
tech.root: SecCertEnroll
ms.assetid: 7aef6c1e-c3f1-4124-b397-bf13ca610135
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EncryptionAlgorithm property [Security], EncryptionAlgorithm property [Security],IX509AttributeArchiveKey interface, IX509AttributeArchiveKey interface [Security],EncryptionAlgorithm property, IX509AttributeArchiveKey.EncryptionAlgorithm, IX509AttributeArchiveKey.get_EncryptionAlgorithm, IX509AttributeArchiveKey::EncryptionAlgorithm, IX509AttributeArchiveKey::get_EncryptionAlgorithm, certenroll/IX509AttributeArchiveKey::EncryptionAlgorithm, certenroll/IX509AttributeArchiveKey::get_EncryptionAlgorithm, get_EncryptionAlgorithm, security.ix509attributearchivekey_encryptionalgorithm_property
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
 - IX509AttributeArchiveKey.EncryptionAlgorithm
 - IX509AttributeArchiveKey.get_EncryptionAlgorithm
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509AttributeArchiveKey::get_EncryptionAlgorithm


## -description


The <b>EncryptionAlgorithm</b> property retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) of the symmetric encryption algorithm used to encrypt the <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">private key</a>.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/en-us/library/Aa377070(v=VS.85).aspx">InitializeEncode</a> method or the  <a href="https://msdn.microsoft.com/en-us/library/Aa377069(v=VS.85).aspx">InitializeDecode</a> method to initialize the <b>EncryptionAlgorithm</b> property. You can call the following properties to retrieve the raw data:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377066(v=VS.85).aspx">EncryptedKeyBlob</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377068(v=VS.85).aspx">EncryptionStrength</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377059(v=VS.85).aspx">IX509AttributeArchiveKey</a>
 

 

