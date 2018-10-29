---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_X509Extensions
title: IX509CertificateRequestPkcs10::get_X509Extensions
author: windows-sdk-content
description: Retrieves a collection of the extensions included in the certificate request.
old-location: security\ix509certificaterequestpkcs10_x509extensions_property.htm
tech.root: SecCertEnroll
ms.assetid: b5500c94-7d7a-473d-80ef-c0d713dcb52e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],X509Extensions property, IX509CertificateRequestPkcs10.X509Extensions, IX509CertificateRequestPkcs10.get_X509Extensions, IX509CertificateRequestPkcs10::X509Extensions, IX509CertificateRequestPkcs10::get_X509Extensions, X509Extensions property [Security], X509Extensions property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::X509Extensions, certenroll/IX509CertificateRequestPkcs10::get_X509Extensions, get_X509Extensions, security.ix509certificaterequestpkcs10_x509extensions_property
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
 - IX509CertificateRequestPkcs10.X509Extensions
 - IX509CertificateRequestPkcs10.get_X509Extensions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestPkcs10::get_X509Extensions


## -description


The <b>X509Extensions</b> property retrieves a collection of the extensions included in the certificate request. This property is web enabled.

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
 

 

