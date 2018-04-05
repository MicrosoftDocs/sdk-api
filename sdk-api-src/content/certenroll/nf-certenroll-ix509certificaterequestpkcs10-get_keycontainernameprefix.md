---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_KeyContainerNamePrefix
title: IX509CertificateRequestPkcs10::get_KeyContainerNamePrefix method
author: windows-driver-content
description: Specifies or retrieves a prefix used to create the container name for a new private key.
old-location: security\ix509certificaterequestpkcs10_keycontainernameprefix_property.htm
old-project: SecCertEnroll
ms.assetid: d4a99b08-5616-4c75-b99f-680f55288baa
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: IX509CertificateRequestPkcs10, IX509CertificateRequestPkcs10 interface [Security], KeyContainerNamePrefix property, IX509CertificateRequestPkcs10.KeyContainerNamePrefix, IX509CertificateRequestPkcs10::get_KeyContainerNamePrefix, IX509CertificateRequestPkcs10::put_KeyContainerNamePrefix, KeyContainerNamePrefix property [Security], KeyContainerNamePrefix property [Security], IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::KeyContainerNamePrefix, certenroll/IX509CertificateRequestPkcs10::get_KeyContainerNamePrefix, certenroll/IX509CertificateRequestPkcs10::put_KeyContainerNamePrefix, get_KeyContainerNamePrefix,IX509CertificateRequestPkcs10.get_KeyContainerNamePrefix, security.ix509certificaterequestpkcs10_keycontainernameprefix_property
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
-	IX509CertificateRequestPkcs10.KeyContainerNamePrefix
-	IX509CertificateRequestPkcs10.get_KeyContainerNamePrefix
-	IX509CertificateRequestPkcs10.put_KeyContainerNamePrefix
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestPkcs10::get_KeyContainerNamePrefix method


## -description


The <b>KeyContainerNamePrefix</b> property specifies or retrieves a prefix used to create the container name for a new private key.

This property is read/write.


## -parameters


## -remarks



Each CryptoAPI <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> or Cryptography API: Next Generation (CNG) key provider maintains a key container for the private key. To retrieve the name of a key container for an existing key, use the <a href="https://msdn.microsoft.com/1d56fa7e-8113-461d-a4f0-ebc048fbcb49">ContainerName</a> property of the <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> object.

A prefix can contain any string limited to the maximum length of the key container name and to legal container name characters. For example, if you do not call the <a href="https://msdn.microsoft.com/1d56fa7e-8113-461d-a4f0-ebc048fbcb49">ContainerName</a> property to specify a key container name, one is automatically created when the private key is created, and the prefix to the container name will be the string "lp". For another example, if you are creating a test harness and want to differentiate key containers by the programs that generated them, you can use the name of the executable as the prefix.

You must set this property before calling the <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a> method, and you must initialize the <a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a> object before calling this property. For more information, see any of the following methods:<ul>
<li>
<a href="https://msdn.microsoft.com/10ab62c3-9c6f-4e1b-8a86-131d08282d9c">InitializeDecode</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3f390abc-5c1c-4f9c-a5f4-4d6fec065acf">InitializeFromCertificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b26e69c4-bfe4-4395-aaf6-bc1d045f59cc">InitializeFromPrivateKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7b7e00dc-649b-4bcb-a9b6-5745b33ea48b">InitializeFromPublicKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4ea746c3-b967-41b4-94ae-7b16b93ca4e4">InitializeFromTemplateName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>
 

 

