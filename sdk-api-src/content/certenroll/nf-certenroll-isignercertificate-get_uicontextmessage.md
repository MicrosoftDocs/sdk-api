---
UID: NF:certenroll.ISignerCertificate.get_UIContextMessage
title: ISignerCertificate::get_UIContextMessage
author: windows-sdk-content
description: Specifies or retrieves a string that contains user interface text associated with the signing certificate.
old-location: security\isignercertificate_uicontextmessage_property.htm
tech.root: SecCertEnroll
ms.assetid: 0fd874b0-9093-4c1b-94a0-a2aaad19010e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ISignerCertificate interface [Security],UIContextMessage property, ISignerCertificate.UIContextMessage, ISignerCertificate.get_UIContextMessage, ISignerCertificate::UIContextMessage, ISignerCertificate::get_UIContextMessage, ISignerCertificate::put_UIContextMessage, UIContextMessage property [Security], UIContextMessage property [Security],ISignerCertificate interface, certenroll/ISignerCertificate::UIContextMessage, certenroll/ISignerCertificate::get_UIContextMessage, certenroll/ISignerCertificate::put_UIContextMessage, get_UIContextMessage, security.isignercertificate_uicontextmessage_property
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
 - ISignerCertificate.UIContextMessage
 - ISignerCertificate.get_UIContextMessage
 - ISignerCertificate.put_UIContextMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- ISignerCertificate.get_UIContextMessage
: 
---

# ISignerCertificate::get_UIContextMessage


## -description


The <b>UIContextMessage</b> property specifies or retrieves a string that contains user interface text associated with the  signing certificate.

This property is read/write.


## -parameters


## -remarks



Call this property to specify a value before calling the <a href="https://msdn.microsoft.com/2553f0bc-a177-49fc-932f-080cb4bd7a5c">Initialize</a> method. You can also call the following properties to retrieve additional information about the signing certificate object:

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
<a href="https://msdn.microsoft.com/047a22ba-9817-45b7-aa9a-356245d2b824">PrivateKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e870e17f-42e4-4548-b876-f5e0556bff0e">SignatureInformation</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b598d4a2-d53a-4091-a059-f9674acf9318">Silent</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a>
 

 

