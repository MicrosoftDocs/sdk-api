---
UID: NF:certenroll.ISignerCertificate.put_Silent
title: ISignerCertificate::put_Silent
author: windows-sdk-content
description: Specifies or retrieves a Boolean value that indicates whether the user is notified when the private key is used to sign a certificate request.
old-location: security\isignercertificate_silent_property.htm
tech.root: SecCertEnroll
ms.assetid: b598d4a2-d53a-4091-a059-f9674acf9318
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ISignerCertificate interface [Security],Silent property, ISignerCertificate.Silent, ISignerCertificate.put_Silent, ISignerCertificate::Silent, ISignerCertificate::get_Silent, ISignerCertificate::put_Silent, Silent property [Security], Silent property [Security],ISignerCertificate interface, certenroll/ISignerCertificate::Silent, certenroll/ISignerCertificate::get_Silent, certenroll/ISignerCertificate::put_Silent, put_Silent, security.isignercertificate_silent_property
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
 - ISignerCertificate.Silent
 - ISignerCertificate.get_Silent
 - ISignerCertificate.put_Silent
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
- ISignerCertificate.put_Silent
: 
---

# ISignerCertificate::put_Silent


## -description


The <b>Silent</b> property specifies or retrieves a Boolean value that indicates whether the user is notified when the private key is used to sign a certificate request.

This property is read/write.


## -parameters


## -remarks



Call this property to specify a value before calling the <a href="https://msdn.microsoft.com/en-us/library/Aa376832(v=VS.85).aspx">Initialize</a> method. Setting this property also sets the <a href="https://msdn.microsoft.com/en-us/library/Aa379035(v=VS.85).aspx">Silent</a> property on the <a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a> object. You can retrieve the private key object by calling <a href="https://msdn.microsoft.com/en-us/library/Aa376836(v=VS.85).aspx">PrivateKey</a>. You can call the following properties to retrieve additional information about the signing certificate object:

<ul>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa376838(v=VS.85).aspx">SignatureInformation</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376840(v=VS.85).aspx">UIContextMessage</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376820(v=VS.85).aspx">ISignerCertificate</a>
 

 

