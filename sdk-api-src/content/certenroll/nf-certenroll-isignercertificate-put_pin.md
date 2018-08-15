---
UID: NF:certenroll.ISignerCertificate.put_Pin
title: ISignerCertificate::put_Pin
author: windows-sdk-content
description: Specifies a personal identification number (PIN) used to authenticate a smart card user.
old-location: security\isignercertificate_pin_property.htm
old-project: seccertenroll
ms.assetid: 695d895e-0646-4a2e-a699-86674f919bad
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISignerCertificate interface [Security],Pin property, ISignerCertificate.Pin, ISignerCertificate.put_Pin, ISignerCertificate::Pin, ISignerCertificate::put_Pin, Pin property [Security], Pin property [Security],ISignerCertificate interface, certenroll/ISignerCertificate::Pin, certenroll/ISignerCertificate::put_Pin, put_Pin, security.isignercertificate_pin_property
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
 - ISignerCertificate.Pin
 - ISignerCertificate.put_Pin
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ISignerCertificate::put_Pin


## -description


The <b>Pin</b> property specifies a personal identification number (PIN) used to  authenticate a smart card user. A user must be authenticated before accessing the private key container on the smart card.

This property is write-only.


## -parameters


## -remarks



Call this property to specify a value before calling the <a href="https://msdn.microsoft.com/2553f0bc-a177-49fc-932f-080cb4bd7a5c">Initialize</a> method. The <b>Pin</b> property internally sets the pin number on the  <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> object. You can retrieve the private key object by calling <a href="https://msdn.microsoft.com/047a22ba-9817-45b7-aa9a-356245d2b824">PrivateKey</a>. You can call the following properties to retrieve additional information about the signing certificate object:

<ul>
<li>
<a href="https://msdn.microsoft.com/7c7cc326-593d-4b2b-b8db-46aaf894279b">Certificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a1749c92-11e4-4726-a355-ccdd245b4df8">ParentWindow</a>
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
 

 

