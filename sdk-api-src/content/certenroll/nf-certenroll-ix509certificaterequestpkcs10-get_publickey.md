---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_PublicKey
title: IX509CertificateRequestPkcs10::get_PublicKey
author: windows-sdk-content
description: Retrieves the IX509PublicKey object that contains the public key included in the certificate request.
old-location: security\ix509certificaterequestpkcs10_publickey_property.htm
tech.root: seccertenroll
ms.assetid: 9f9d05d8-9bc5-441e-8409-498ee9d20c25
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],PublicKey property, IX509CertificateRequestPkcs10.PublicKey, IX509CertificateRequestPkcs10.get_PublicKey, IX509CertificateRequestPkcs10::PublicKey, IX509CertificateRequestPkcs10::get_PublicKey, PublicKey property [Security], PublicKey property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::PublicKey, certenroll/IX509CertificateRequestPkcs10::get_PublicKey, get_PublicKey, security.ix509certificaterequestpkcs10_publickey_property
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
 - IX509CertificateRequestPkcs10.PublicKey
 - IX509CertificateRequestPkcs10.get_PublicKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestPkcs10::get_PublicKey


## -description


The <b>PublicKey</b> property retrieves the <a href="https://msdn.microsoft.com/en-us/library/Aa379039(v=VS.85).aspx">IX509PublicKey</a> object that contains the public key included in the certificate request.

This property is read-only.


## -parameters


## -remarks



 You must initialize the <a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a> object before calling this property. For more information, see any of the following methods:<ul>
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
 

 

