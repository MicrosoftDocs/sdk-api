---
UID: NF:certenroll.IX509PublicKey.get_EncodedKey
title: IX509PublicKey::get_EncodedKey (certenroll.h)
author: windows-sdk-content
description: Retrieves a byte array that contains the public key.
old-location: security\ix509publickey_encodedkey_property.htm
tech.root: seccertenroll
ms.assetid: 3573f4b6-ecfd-4540-bc43-c88943992fe2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EncodedKey property [Security], EncodedKey property [Security],IX509PublicKey interface, IX509PublicKey interface [Security],EncodedKey property, IX509PublicKey.EncodedKey, IX509PublicKey.get_EncodedKey, IX509PublicKey::EncodedKey, IX509PublicKey::get_EncodedKey, certenroll/IX509PublicKey::EncodedKey, certenroll/IX509PublicKey::get_EncodedKey, get_EncodedKey, security.ix509publickey_encodedkey_property
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
 - IX509PublicKey.EncodedKey
 - IX509PublicKey.get_EncodedKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509PublicKey::get_EncodedKey


## -description


The <b>EncodedKey</b> property retrieves a byte array that contains the public key.  The byte array is represented by a Unicode-encoded string.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/3e92d934-1ab7-4f09-a579-0dde4ef44c7f">InitializeFromEncodedPublicKeyInfo</a> method or the <a href="https://msdn.microsoft.com/b6db46b2-95f5-4ba9-829d-97bf83fd9806">Initialize</a> method to initialize the public key object before calling this property.




## -see-also




<a href="https://msdn.microsoft.com/cd6f28a3-9998-40d7-a3e8-dab0cf3991a8">IX509PublicKey</a>
 

 

