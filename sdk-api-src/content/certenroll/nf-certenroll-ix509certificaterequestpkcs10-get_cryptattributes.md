---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_CryptAttributes
title: IX509CertificateRequestPkcs10::get_CryptAttributes
author: windows-sdk-content
description: Retrieves an ICryptAttributes collection of optional certificate attributes.
old-location: security\ix509certificaterequestpkcs10_cryptattributes_property.htm
tech.root: seccertenroll
ms.assetid: 078b6c55-8b56-4075-a8fa-b3230041ded0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CryptAttributes property [Security], CryptAttributes property [Security],IX509CertificateRequestPkcs10 interface, IX509CertificateRequestPkcs10 interface [Security],CryptAttributes property, IX509CertificateRequestPkcs10.CryptAttributes, IX509CertificateRequestPkcs10.get_CryptAttributes, IX509CertificateRequestPkcs10::CryptAttributes, IX509CertificateRequestPkcs10::get_CryptAttributes, certenroll/IX509CertificateRequestPkcs10::CryptAttributes, certenroll/IX509CertificateRequestPkcs10::get_CryptAttributes, get_CryptAttributes, security.ix509certificaterequestpkcs10_cryptattributes_property
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
 - IX509CertificateRequestPkcs10.CryptAttributes
 - IX509CertificateRequestPkcs10.get_CryptAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestPkcs10::get_CryptAttributes


## -description


The <b>CryptAttributes</b> property retrieves an <a href="https://msdn.microsoft.com/beedb57c-1c89-4d16-8514-046e3071fd1e">ICryptAttributes</a> collection of optional certificate attributes.

This property is read-only.


## -parameters


## -remarks



 You must initialize the <a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a> object before calling this property. For more information, see any of the following methods:

<ul>
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
 

 

