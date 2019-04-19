---
UID: NF:certenroll.ISignerCertificate.put_Silent
title: ISignerCertificate::put_Silent (certenroll.h)
author: windows-sdk-content
description: Specifies or retrieves a Boolean value that indicates whether the user is notified when the private key is used to sign a certificate request.
old-location: security\isignercertificate_silent_property.htm
tech.root: seccertenroll
ms.assetid: b598d4a2-d53a-4091-a059-f9674acf9318
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISignerCertificate interface [Security],Silent property, ISignerCertificate.Silent, ISignerCertificate.put_Silent, ISignerCertificate::Silent, ISignerCertificate::get_Silent, ISignerCertificate::put_Silent, Silent property [Security], Silent property [Security],ISignerCertificate interface, certenroll/ISignerCertificate::Silent, certenroll/ISignerCertificate::get_Silent, certenroll/ISignerCertificate::put_Silent, put_Silent, security.isignercertificate_silent_property
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
 - ISignerCertificate.Silent
 - ISignerCertificate.get_Silent
 - ISignerCertificate.put_Silent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISignerCertificate::put_Silent


## -description


The <b>Silent</b> property specifies or retrieves a Boolean value that indicates whether the user is notified when the private key is used to sign a certificate request.

This property is read/write.


## -parameters


## -remarks



Call this property to specify a value before calling the <a href="https://msdn.microsoft.com/2553f0bc-a177-49fc-932f-080cb4bd7a5c">Initialize</a> method. Setting this property also sets the <a href="https://msdn.microsoft.com/4f61a513-620c-48c4-b9dd-032b13a9f654">Silent</a> property on the <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> object. You can retrieve the private key object by calling <a href="https://msdn.microsoft.com/047a22ba-9817-45b7-aa9a-356245d2b824">PrivateKey</a>. You can call the following properties to retrieve additional information about the signing certificate object:

<ul>
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
<a href="https://msdn.microsoft.com/e870e17f-42e4-4548-b876-f5e0556bff0e">SignatureInformation</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0fd874b0-9093-4c1b-94a0-a2aaad19010e">UIContextMessage</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a>
 

 

