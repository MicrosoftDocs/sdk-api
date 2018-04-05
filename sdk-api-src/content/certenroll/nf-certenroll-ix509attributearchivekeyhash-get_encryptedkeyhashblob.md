---
UID: NF:certenroll.IX509AttributeArchiveKeyHash.get_EncryptedKeyHashBlob
title: IX509AttributeArchiveKeyHash::get_EncryptedKeyHashBlob method
author: windows-driver-content
description: Retrieves a string that contains a hash of the encrypted private key.
old-location: security\ix509attributearchivekeyhash_encryptedkeyhashblob_property.htm
old-project: SecCertEnroll
ms.assetid: ff75aaf8-1544-465b-af0d-620ca6984249
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: EncryptedKeyHashBlob property [Security], EncryptedKeyHashBlob property [Security], IX509AttributeArchiveKeyHash interface, IX509AttributeArchiveKeyHash, IX509AttributeArchiveKeyHash interface [Security], EncryptedKeyHashBlob property, IX509AttributeArchiveKeyHash.EncryptedKeyHashBlob, IX509AttributeArchiveKeyHash::get_EncryptedKeyHashBlob, certenroll/IX509AttributeArchiveKeyHash::EncryptedKeyHashBlob, certenroll/IX509AttributeArchiveKeyHash::get_EncryptedKeyHashBlob, get_EncryptedKeyHashBlob,IX509AttributeArchiveKeyHash.get_EncryptedKeyHashBlob, security.ix509attributearchivekeyhash_encryptedkeyhashblob_property
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
-	IX509AttributeArchiveKeyHash.EncryptedKeyHashBlob
-	IX509AttributeArchiveKeyHash.get_EncryptedKeyHashBlob
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509AttributeArchiveKeyHash::get_EncryptedKeyHashBlob method


## -description


The <b>EncryptedKeyHashBlob</b> property retrieves a string that contains a <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> of the encrypted <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a>.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/2101f15f-b71b-4dea-8ec8-2d3c1926ae15">InitializeEncodeFromEncryptedKeyBlob</a> method or the  <a href="https://msdn.microsoft.com/c8f59fba-c6ce-4e11-bb25-8a6fd23218d1">InitializeDecode</a> method to initialize the <b>EncryptedKeyHashBlob</b> property.




## -see-also




<a href="https://msdn.microsoft.com/52c92629-4c9e-4996-80a2-30e2212b3009">IX509AttributeArchiveKeyHash</a>
 

 

