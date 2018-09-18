---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_SuppressOids
title: IX509CertificateRequestPkcs10::get_SuppressOids
author: windows-sdk-content
description: Retrieves a collection of the default extension and attribute object identifiers (OIDs) that were not added to the request when the request was encoded.
old-location: security\ix509certificaterequestpkcs10_suppressoids_property.htm
tech.root: seccertenroll
ms.assetid: 3f7a6d23-00d3-4ab6-817a-a37490f0cb84
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],SuppressOids property, IX509CertificateRequestPkcs10.SuppressOids, IX509CertificateRequestPkcs10.get_SuppressOids, IX509CertificateRequestPkcs10::SuppressOids, IX509CertificateRequestPkcs10::get_SuppressOids, SuppressOids property [Security], SuppressOids property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::SuppressOids, certenroll/IX509CertificateRequestPkcs10::get_SuppressOids, get_SuppressOids, security.ix509certificaterequestpkcs10_suppressoids_property
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
 - IX509CertificateRequestPkcs10.SuppressOids
 - IX509CertificateRequestPkcs10.get_SuppressOids
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestPkcs10::get_SuppressOids


## -description


The <b>SuppressOids</b> property retrieves a collection of the default extension and attribute <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifiers</a> (OIDs) that were not added  to the request when the request was encoded.

This property is read-only.


## -parameters


## -remarks



Attributes and extensions are added to a certificate request when it is encoded or initialized. You can suppress the addition of default extensions and attributes by calling the <a href="https://msdn.microsoft.com/en-us/library/Aa377698(v=VS.85).aspx">SuppressDefaults</a> property. For a PKCS #10 request, the following attributes are added by default:

<ul>
<li>XCN_OID_REQUEST_CLIENT_INFO
(<a href="https://msdn.microsoft.com/en-us/library/Aa377073(v=VS.85).aspx">IX509AttributeClientId</a>)</li>
<li>XCN_OID_ENROLLMENT_CSP_PROVIDER (<a href="https://msdn.microsoft.com/en-us/library/Aa377082(v=VS.85).aspx">IX509AttributeCspProvider</a>)</li>
<li>XCN_OID_OS_VERSION (<a href="https://msdn.microsoft.com/en-us/library/Aa377096(v=VS.85).aspx">IX509AttributeOSVersion</a>)</li>
<li>XCN_OID_RENEWAL_CERTIFICATE (<a href="https://msdn.microsoft.com/en-us/library/Aa377102(v=VS.85).aspx">IX509AttributeRenewalCertificate</a>)</li>
</ul>
The following extensions are added by default:<ul>
<li>XCN_OID_RSA_SMIMECapabilities (<a href="https://msdn.microsoft.com/en-us/library/Aa378177(v=VS.85).aspx">IX509ExtensionSmimeCapabilities</a>)</li>
<li>XCN_OID_SUBJECT_KEY_IDENTIFIER
(<a href="https://msdn.microsoft.com/en-us/library/Aa378215(v=VS.85).aspx">IX509ExtensionSubjectKeyIdentifier</a>)</li>
<li>XCN_OID_KEY_USAGE (<a href="https://msdn.microsoft.com/en-us/library/Aa378144(v=VS.85).aspx">IX509ExtensionKeyUsage</a>)</li>
</ul>


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




<a href="https://msdn.microsoft.com/en-us/library/Aa375929(v=VS.85).aspx">ICryptAttribute</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa378077(v=VS.85).aspx">IX509Extension</a>
 

 

