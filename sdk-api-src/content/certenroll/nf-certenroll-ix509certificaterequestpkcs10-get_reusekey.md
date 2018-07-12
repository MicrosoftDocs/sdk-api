---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_ReuseKey
title: IX509CertificateRequestPkcs10::get_ReuseKey
author: windows-sdk-content
description: Retrieves a Boolean value that indicates whether an existing private key was used to sign the request.
old-location: security\ix509certificaterequestpkcs10_reusekey_property.htm
old-project: seccertenroll
ms.assetid: b6788885-1036-4edd-bbb9-4d9808771d95
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],ReuseKey property, IX509CertificateRequestPkcs10.ReuseKey, IX509CertificateRequestPkcs10.get_ReuseKey, IX509CertificateRequestPkcs10::ReuseKey, IX509CertificateRequestPkcs10::get_ReuseKey, ReuseKey property [Security], ReuseKey property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::ReuseKey, certenroll/IX509CertificateRequestPkcs10::get_ReuseKey, get_ReuseKey, security.ix509certificaterequestpkcs10_reusekey_property
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509CertificateRequestPkcs10.ReuseKey
 - IX509CertificateRequestPkcs10.get_ReuseKey
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestPkcs10::get_ReuseKey


## -description


The <b>ReuseKey</b> property retrieves a Boolean value that indicates whether an existing private key was used to sign the request.

This property is read-only.


## -parameters


## -remarks



If you initialized the request object by calling the <a href="https://msdn.microsoft.com/3f390abc-5c1c-4f9c-a5f4-4d6fec065acf">InitializeFromCertificate</a> method, you specified a value for the <i>InheritOptions</i> parameter that indicated whether the private key used to sign the request was inherited from the certificate. If you specified <b>InheritPrivateKey</b> for this parameter, the <b>ReuseKey</b> property returns a value of Boolean true.




## -see-also




<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>
 

 

