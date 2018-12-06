---
UID: NF:certenroll.IX509AttributeRenewalCertificate.get_RenewalCertificate
title: IX509AttributeRenewalCertificate::get_RenewalCertificate
author: windows-sdk-content
description: Retrieves the certificate to be renewed.
old-location: security\ix509attributerenewalcertificate_renewalcertificate_property.htm
tech.root: seccertenroll
ms.assetid: 5c7997de-9abb-4a96-b906-a6de7378d0b1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IX509AttributeRenewalCertificate interface [Security],RenewalCertificate property, IX509AttributeRenewalCertificate.RenewalCertificate, IX509AttributeRenewalCertificate.get_RenewalCertificate, IX509AttributeRenewalCertificate::RenewalCertificate, IX509AttributeRenewalCertificate::get_RenewalCertificate, RenewalCertificate property [Security], RenewalCertificate property [Security],IX509AttributeRenewalCertificate interface, certenroll/IX509AttributeRenewalCertificate::RenewalCertificate, certenroll/IX509AttributeRenewalCertificate::get_RenewalCertificate, get_RenewalCertificate, security.ix509attributerenewalcertificate_renewalcertificate_property
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
 - IX509AttributeRenewalCertificate.RenewalCertificate
 - IX509AttributeRenewalCertificate.get_RenewalCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509AttributeRenewalCertificate::get_RenewalCertificate


## -description


The <b>RenewalCertificate</b> property retrieves the certificate to be renewed. The <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded certificate is contained in a byte array that is represented by a Unicode-encoded string.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/a234755e-5b90-43f1-81f2-c2ebec9b55a4">InitializeEncode</a> method or the  <a href="https://msdn.microsoft.com/dd5a43c3-5244-43da-a6d5-87b109baea09">InitializeDecode</a> method to initialize the <b>RenewalCertificate</b> property.




## -see-also




<a href="https://msdn.microsoft.com/fc432a7a-6ef7-4359-bb53-1ed5df6bc0ab">IX509AttributeRenewalCertificate</a>
 

 

