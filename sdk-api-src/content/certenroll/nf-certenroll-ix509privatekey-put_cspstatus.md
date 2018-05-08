---
UID: NF:certenroll.IX509PrivateKey.put_CspStatus
title: IX509PrivateKey::put_CspStatus
author: windows-driver-content
description: Specifies or retrieves an ICspStatus object that contains information about the cryptographic provider and algorithm pair associated with the private key.
old-location: security\ix509privatekey_cspstatus.htm
old-project: SecCertEnroll
ms.assetid: 8bf6e62d-9ecf-4eee-9652-f04d2010b4f7
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: CspStatus property [Security], CspStatus property [Security],IX509PrivateKey interface, IX509PrivateKey interface [Security],CspStatus property, IX509PrivateKey.CspStatus, IX509PrivateKey.put_CspStatus, IX509PrivateKey::CspStatus, IX509PrivateKey::get_CspStatus, IX509PrivateKey::put_CspStatus, certenroll/IX509PrivateKey::CspStatus, certenroll/IX509PrivateKey::get_CspStatus, certenroll/IX509PrivateKey::put_CspStatus, put_CspStatus, security.ix509privatekey_cspstatus
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
-	IX509PrivateKey.CspStatus
-	IX509PrivateKey.get_CspStatus
-	IX509PrivateKey.put_CspStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509PrivateKey::put_CspStatus


## -description


The <b>CspStatus</b> property specifies or retrieves an <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> object that contains information about the cryptographic provider and algorithm pair associated with the private key. This property is web enabled for both input and output.

This property is read/write.


## -parameters


## -remarks



The <a href="https://msdn.microsoft.com/40d2eae1-733a-4e5b-bb15-71301d73f438">Algorithm</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/dn915743">ProviderName</a> properties are automatically set when you call the <b>CspStatus</b> property. The <b>CspStatus</b> property is typically set during the enrollment process. That is, when a request template specifies multiple provider/algorithm pairs, the enrollment code sets the <b>CspStatus</b> property to the first enabled <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> object and tries to create a private key. If a key cannot be created, the enrollment code sets this property to the next enabled <b>ICspStatus</b> object and tries again.




## -see-also




<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
 

 

