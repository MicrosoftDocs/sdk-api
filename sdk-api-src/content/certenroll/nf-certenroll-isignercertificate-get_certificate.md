---
UID: NF:certenroll.ISignerCertificate.get_Certificate
title: ISignerCertificate::get_Certificate (certenroll.h)
author: windows-sdk-content
description: Retrieves a Distinguished Encoding Rules (DER) encoded byte array that contains the certificate.
old-location: security\isignercertificate_certificate_property.htm
tech.root: seccertenroll
ms.assetid: 7c7cc326-593d-4b2b-b8db-46aaf894279b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Certificate property [Security], Certificate property [Security],ISignerCertificate interface, ISignerCertificate interface [Security],Certificate property, ISignerCertificate.Certificate, ISignerCertificate.get_Certificate, ISignerCertificate::Certificate, ISignerCertificate::get_Certificate, certenroll/ISignerCertificate::Certificate, certenroll/ISignerCertificate::get_Certificate, get_Certificate, security.isignercertificate_certificate_property
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
 - ISignerCertificate.Certificate
 - ISignerCertificate.get_Certificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISignerCertificate::get_Certificate


## -description


The <b>Certificate</b> property retrieves a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the certificate. The DER-encoded byte array is represented by a Unicode-encoded string.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/2553f0bc-a177-49fc-932f-080cb4bd7a5c">Initialize</a> method to specify the certificate. You can also call the following properties to retrieve information about the signing certificate object:

<ul>
<li>
<a href="https://msdn.microsoft.com/695d895e-0646-4a2e-a699-86674f919bad">Pin</a>
</li>
<li>
<a href="https://msdn.microsoft.com/047a22ba-9817-45b7-aa9a-356245d2b824">PrivateKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e870e17f-42e4-4548-b876-f5e0556bff0e">SignatureInformation</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b598d4a2-d53a-4091-a059-f9674acf9318">Silent</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0fd874b0-9093-4c1b-94a0-a2aaad19010e">UIContextMessage</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a>
 

 

