---
UID: NF:certenroll.ISignerCertificate.get_SignatureInformation
title: ISignerCertificate::get_SignatureInformation
author: windows-sdk-content
description: Retrieves an IX509SignatureInformation object that contains information about the certificate signature.
old-location: security\isignercertificate_signatureinformation_property.htm
old-project: seccertenroll
ms.assetid: e870e17f-42e4-4548-b876-f5e0556bff0e
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISignerCertificate interface [Security],SignatureInformation property, ISignerCertificate.SignatureInformation, ISignerCertificate.get_SignatureInformation, ISignerCertificate::SignatureInformation, ISignerCertificate::get_SignatureInformation, SignatureInformation property [Security], SignatureInformation property [Security],ISignerCertificate interface, certenroll/ISignerCertificate::SignatureInformation, certenroll/ISignerCertificate::get_SignatureInformation, get_SignatureInformation, security.isignercertificate_signatureinformation_property
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.redist: 
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
 - ISignerCertificate.SignatureInformation
 - ISignerCertificate.get_SignatureInformation
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ISignerCertificate::get_SignatureInformation


## -description


The <b>SignatureInformation</b> property retrieves an <a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a> object that contains information about the certificate signature.

This property is read-only.


## -parameters


## -remarks



When you call the <a href="https://msdn.microsoft.com/en-us/library/Aa376832(v=VS.85).aspx">Initialize</a> method the Certificate Enrollment Control creates an <a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a> object. You can also call the following properties to retrieve information about the signing certificate object:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376831(v=VS.85).aspx">Certificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376834(v=VS.85).aspx">ParentWindow</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376835(v=VS.85).aspx">Pin</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376836(v=VS.85).aspx">PrivateKey</a>
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
 

 

