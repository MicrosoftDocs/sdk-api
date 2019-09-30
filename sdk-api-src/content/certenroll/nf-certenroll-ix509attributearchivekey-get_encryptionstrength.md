---
UID: NF:certenroll.IX509AttributeArchiveKey.get_EncryptionStrength
title: IX509AttributeArchiveKey::get_EncryptionStrength (certenroll.h)
author: windows-sdk-content
description: Retrieves an integer that contains the encryption strength of the symmetric algorithm used to encrypt the key.
old-location: security\ix509attributearchivekey_encryptionstrength_property.htm
tech.root: seccertenroll
ms.assetid: c365a2e0-caff-4c92-aa22-33c165ea672e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EncryptionStrength property [Security], EncryptionStrength property [Security],IX509AttributeArchiveKey interface, IX509AttributeArchiveKey interface [Security],EncryptionStrength property, IX509AttributeArchiveKey.EncryptionStrength, IX509AttributeArchiveKey.get_EncryptionStrength, IX509AttributeArchiveKey::EncryptionStrength, IX509AttributeArchiveKey::get_EncryptionStrength, certenroll/IX509AttributeArchiveKey::EncryptionStrength, certenroll/IX509AttributeArchiveKey::get_EncryptionStrength, get_EncryptionStrength, security.ix509attributearchivekey_encryptionstrength_property
ms.topic: method
f1_keywords: 
 - "certenroll/IX509AttributeArchiveKey.EncryptionStrength"
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
 - IX509AttributeArchiveKey.EncryptionStrength
 - IX509AttributeArchiveKey.get_EncryptionStrength
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509AttributeArchiveKey::get_EncryptionStrength


## -description


The <b>EncryptionStrength</b> property retrieves an integer that contains the encryption strength of the symmetric algorithm used to encrypt the key.

This property is read-only.


## -parameters


## -remarks



You can specify this property by calling the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekey-initializeencode">InitializeEncode</a> method or the  <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekey-initializedecode">InitializeDecode</a> method. However, the property is currently ignored and zero is returned because the Certificate Enrollment SDK does not support any algorithms for which the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) does not already imply the encryption strength (key length). For example, AES has multiple strengths, but each strength is already indicated by the OID. 

You can call the following properties to retrieve the raw data:<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekey-get_encryptionalgorithm">EncryptionAlgorithm</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekey-get_encryptedkeyblob">EncryptedKeyBlob</a>
</li>
</ul>





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributearchivekey">IX509AttributeArchiveKey</a>
 

 

