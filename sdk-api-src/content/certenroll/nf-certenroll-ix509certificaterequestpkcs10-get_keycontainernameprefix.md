---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_KeyContainerNamePrefix
title: IX509CertificateRequestPkcs10::get_KeyContainerNamePrefix
author: windows-sdk-content
description: Specifies or retrieves a prefix used to create the container name for a new private key.
old-location: security\ix509certificaterequestpkcs10_keycontainernameprefix_property.htm
tech.root: SecCertEnroll
ms.assetid: d4a99b08-5616-4c75-b99f-680f55288baa
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],KeyContainerNamePrefix property, IX509CertificateRequestPkcs10.KeyContainerNamePrefix, IX509CertificateRequestPkcs10.get_KeyContainerNamePrefix, IX509CertificateRequestPkcs10::KeyContainerNamePrefix, IX509CertificateRequestPkcs10::get_KeyContainerNamePrefix, IX509CertificateRequestPkcs10::put_KeyContainerNamePrefix, KeyContainerNamePrefix property [Security], KeyContainerNamePrefix property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::KeyContainerNamePrefix, certenroll/IX509CertificateRequestPkcs10::get_KeyContainerNamePrefix, certenroll/IX509CertificateRequestPkcs10::put_KeyContainerNamePrefix, get_KeyContainerNamePrefix, security.ix509certificaterequestpkcs10_keycontainernameprefix_property
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
 - IX509CertificateRequestPkcs10.KeyContainerNamePrefix
 - IX509CertificateRequestPkcs10.get_KeyContainerNamePrefix
 - IX509CertificateRequestPkcs10.put_KeyContainerNamePrefix
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
- IX509CertificateRequestPkcs10.get_KeyContainerNamePrefix
: 
---

# IX509CertificateRequestPkcs10::get_KeyContainerNamePrefix


## -description


The <b>KeyContainerNamePrefix</b> property specifies or retrieves a prefix used to create the container name for a new private key.

This property is read/write.


## -parameters


## -remarks



Each CryptoAPI <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">cryptographic service provider</a> or Cryptography API: Next Generation (CNG) key provider maintains a key container for the private key. To retrieve the name of a key container for an existing key, use the <a href="https://msdn.microsoft.com/en-us/library/Aa378953(v=VS.85).aspx">ContainerName</a> property of the <a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a> object.

A prefix can contain any string limited to the maximum length of the key container name and to legal container name characters. For example, if you do not call the <a href="https://msdn.microsoft.com/en-us/library/Aa378953(v=VS.85).aspx">ContainerName</a> property to specify a key container name, one is automatically created when the private key is created, and the prefix to the container name will be the string "lp". For another example, if you are creating a test harness and want to differentiate key containers by the programs that generated them, you can use the name of the executable as the prefix.

You must set this property before calling the <a href="https://msdn.microsoft.com/en-us/library/Aa377650(v=VS.85).aspx">Encode</a> method, and you must initialize the <a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a> object before calling this property. For more information, see any of the following methods:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377520(v=VS.85).aspx">InitializeDecode</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377523(v=VS.85).aspx">InitializeFromCertificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377527(v=VS.85).aspx">InitializeFromPrivateKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377531(v=VS.85).aspx">InitializeFromPublicKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377533(v=VS.85).aspx">InitializeFromTemplateName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>
 

 

