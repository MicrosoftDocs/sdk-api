---
UID: NF:certenroll.ISignerCertificate.get_Certificate
title: ISignerCertificate::get_Certificate
author: windows-sdk-content
description: Retrieves a Distinguished Encoding Rules (DER) encoded byte array that contains the certificate.
old-location: security\isignercertificate_certificate_property.htm
tech.root: seccertenroll
ms.assetid: 7c7cc326-593d-4b2b-b8db-46aaf894279b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Certificate property [Security], Certificate property [Security],ISignerCertificate interface, ISignerCertificate interface [Security],Certificate property, ISignerCertificate.Certificate, ISignerCertificate.get_Certificate, ISignerCertificate::Certificate, ISignerCertificate::get_Certificate, certenroll/ISignerCertificate::Certificate, certenroll/ISignerCertificate::get_Certificate, get_Certificate, security.isignercertificate_certificate_property
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
 - ISignerCertificate.Certificate
 - ISignerCertificate.get_Certificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISignerCertificate::get_Certificate


## -description


The <b>Certificate</b> property retrieves a <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the certificate. The DER-encoded byte array is represented by a Unicode-encoded string.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/en-us/library/Aa376832(v=VS.85).aspx">Initialize</a> method to specify the certificate. You can also call the following properties to retrieve information about the signing certificate object:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376835(v=VS.85).aspx">Pin</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376836(v=VS.85).aspx">PrivateKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376838(v=VS.85).aspx">SignatureInformation</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376839(v=VS.85).aspx">Silent</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376840(v=VS.85).aspx">UIContextMessage</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376820(v=VS.85).aspx">ISignerCertificate</a>
 

 

