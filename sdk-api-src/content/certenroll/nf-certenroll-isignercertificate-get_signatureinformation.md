---
UID: NF:certenroll.ISignerCertificate.get_SignatureInformation
title: ISignerCertificate::get_SignatureInformation
author: windows-sdk-content
description: Retrieves an IX509SignatureInformation object that contains information about the certificate signature.
old-location: security\isignercertificate_signatureinformation_property.htm
old-project: SecCertEnroll
ms.assetid: e870e17f-42e4-4548-b876-f5e0556bff0e
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ISignerCertificate interface [Security],SignatureInformation property, ISignerCertificate.SignatureInformation, ISignerCertificate.get_SignatureInformation, ISignerCertificate::SignatureInformation, ISignerCertificate::get_SignatureInformation, SignatureInformation property [Security], SignatureInformation property [Security],ISignerCertificate interface, certenroll/ISignerCertificate::SignatureInformation, certenroll/ISignerCertificate::get_SignatureInformation, get_SignatureInformation, security.isignercertificate_signatureinformation_property
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	ISignerCertificate.SignatureInformation
-	ISignerCertificate.get_SignatureInformation
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ISignerCertificate::get_SignatureInformation


## -description


The <b>SignatureInformation</b> property retrieves an <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a> object that contains information about the certificate signature.

This property is read-only.


## -parameters


## -remarks



When you call the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> method the Certificate Enrollment Control creates an <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a> object. You can also call the following properties to retrieve information about the signing certificate object:<ul>
<li>
<a href="https://msdn.microsoft.com/7c7cc326-593d-4b2b-b8db-46aaf894279b">Certificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a1749c92-11e4-4726-a355-ccdd245b4df8">ParentWindow</a>
</li>
<li>
<a href="https://msdn.microsoft.com/695d895e-0646-4a2e-a699-86674f919bad">Pin</a>
</li>
<li>
<a href="https://msdn.microsoft.com/047a22ba-9817-45b7-aa9a-356245d2b824">PrivateKey</a>
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
 

 

