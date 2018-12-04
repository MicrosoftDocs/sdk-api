---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_TemplateObjectId
title: IX509CertificateRequestPkcs10::get_TemplateObjectId
author: windows-sdk-content
description: Retrieves the object identifier (OID) of the template used to create the certificate request.
old-location: security\ix509certificaterequestpkcs10_templateobjectid_property.htm
tech.root: seccertenroll
ms.assetid: 490a34bc-08b3-4df2-8996-6137bea53420
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],TemplateObjectId property, IX509CertificateRequestPkcs10.TemplateObjectId, IX509CertificateRequestPkcs10.get_TemplateObjectId, IX509CertificateRequestPkcs10::TemplateObjectId, IX509CertificateRequestPkcs10::get_TemplateObjectId, TemplateObjectId property [Security], TemplateObjectId property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::TemplateObjectId, certenroll/IX509CertificateRequestPkcs10::get_TemplateObjectId, get_TemplateObjectId, security.ix509certificaterequestpkcs10_templateobjectid_property
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
 - IX509CertificateRequestPkcs10.TemplateObjectId
 - IX509CertificateRequestPkcs10.get_TemplateObjectId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestPkcs10::get_TemplateObjectId


## -description


The <b>TemplateObjectId</b> property retrieves the  <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) of the template used to create the certificate request.

This property is read-only.


## -parameters


## -remarks



The object identifier can be an OID for the Active Directory Common Name (CN) of the template. You must initialize the <a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a> object before calling this property. For more information, see any of the following methods:<ul>
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
 

 

