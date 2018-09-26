---
UID: NF:certenroll.IX509CertificateRequestCertificate.put_Issuer
title: IX509CertificateRequestCertificate::put_Issuer
author: windows-sdk-content
description: Specifies or retrieves the name of the certificate issuer.
old-location: security\ix509certificaterequestcertificate_issuer_property.htm
tech.root: seccertenroll
ms.assetid: cf07a0ed-8657-4044-8dcd-fcd350af20ee
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IX509CertificateRequestCertificate interface [Security],Issuer property, IX509CertificateRequestCertificate.Issuer, IX509CertificateRequestCertificate.put_Issuer, IX509CertificateRequestCertificate::Issuer, IX509CertificateRequestCertificate::get_Issuer, IX509CertificateRequestCertificate::put_Issuer, Issuer property [Security], Issuer property [Security],IX509CertificateRequestCertificate interface, certenroll/IX509CertificateRequestCertificate::Issuer, certenroll/IX509CertificateRequestCertificate::get_Issuer, certenroll/IX509CertificateRequestCertificate::put_Issuer, put_Issuer, security.ix509certificaterequestcertificate_issuer_property
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
 - IX509CertificateRequestCertificate.Issuer
 - IX509CertificateRequestCertificate.get_Issuer
 - IX509CertificateRequestCertificate.put_Issuer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestCertificate::put_Issuer


## -description


The <b>Issuer</b> property specifies or retrieves the name of the certificate issuer.

This property is read/write.


## -parameters


## -remarks



If you do not specify this property before calling <a href="https://msdn.microsoft.com/en-us/library/Aa377650(v=VS.85).aspx">Encode</a>, the property value is set by using the subject of the signing certificate. If no signing certificate was supplied, the property value is set by using the subject of the request object.

You must initialize the request object before calling this property. For more information, see any of the following methods:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377669(v=VS.85).aspx">Initialize</a>
</li>
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




<a href="https://msdn.microsoft.com/en-us/library/Aa377051(v=VS.85).aspx">IX500DistinguishedName</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377124(v=VS.85).aspx">IX509CertificateRequestCertificate</a>
 

 

