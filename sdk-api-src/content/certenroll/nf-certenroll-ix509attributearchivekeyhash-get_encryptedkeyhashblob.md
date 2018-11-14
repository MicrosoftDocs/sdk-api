---
UID: NF:certenroll.IX509AttributeArchiveKeyHash.get_EncryptedKeyHashBlob
title: IX509AttributeArchiveKeyHash::get_EncryptedKeyHashBlob
author: windows-sdk-content
description: Retrieves a string that contains a hash of the encrypted private key.
old-location: security\ix509attributearchivekeyhash_encryptedkeyhashblob_property.htm
tech.root: SecCertEnroll
ms.assetid: ff75aaf8-1544-465b-af0d-620ca6984249
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EncryptedKeyHashBlob property [Security], EncryptedKeyHashBlob property [Security],IX509AttributeArchiveKeyHash interface, IX509AttributeArchiveKeyHash interface [Security],EncryptedKeyHashBlob property, IX509AttributeArchiveKeyHash.EncryptedKeyHashBlob, IX509AttributeArchiveKeyHash.get_EncryptedKeyHashBlob, IX509AttributeArchiveKeyHash::EncryptedKeyHashBlob, IX509AttributeArchiveKeyHash::get_EncryptedKeyHashBlob, certenroll/IX509AttributeArchiveKeyHash::EncryptedKeyHashBlob, certenroll/IX509AttributeArchiveKeyHash::get_EncryptedKeyHashBlob, get_EncryptedKeyHashBlob, security.ix509attributearchivekeyhash_encryptedkeyhashblob_property
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
 - IX509AttributeArchiveKeyHash.EncryptedKeyHashBlob
 - IX509AttributeArchiveKeyHash.get_EncryptedKeyHashBlob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- IX509AttributeArchiveKeyHash.get_EncryptedKeyHashBlob
: 
---

# IX509AttributeArchiveKeyHash::get_EncryptedKeyHashBlob


## -description


The <b>EncryptedKeyHashBlob</b> property retrieves a string that contains a <a href="https://msdn.microsoft.com/en-us/library/ms721586(v=VS.85).aspx">hash</a> of the encrypted <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">private key</a>.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/en-us/library/Aa377063(v=VS.85).aspx">InitializeEncodeFromEncryptedKeyBlob</a> method or the  <a href="https://msdn.microsoft.com/en-us/library/Aa377062(v=VS.85).aspx">InitializeDecode</a> method to initialize the <b>EncryptedKeyHashBlob</b> property.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377060(v=VS.85).aspx">IX509AttributeArchiveKeyHash</a>
 

 

