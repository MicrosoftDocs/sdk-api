---
UID: NF:certenroll.ISignerCertificate.put_Pin
title: ISignerCertificate::put_Pin
author: windows-sdk-content
description: Specifies a personal identification number (PIN) used to authenticate a smart card user.
old-location: security\isignercertificate_pin_property.htm
tech.root: SecCertEnroll
ms.assetid: 695d895e-0646-4a2e-a699-86674f919bad
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ISignerCertificate interface [Security],Pin property, ISignerCertificate.Pin, ISignerCertificate.put_Pin, ISignerCertificate::Pin, ISignerCertificate::put_Pin, Pin property [Security], Pin property [Security],ISignerCertificate interface, certenroll/ISignerCertificate::Pin, certenroll/ISignerCertificate::put_Pin, put_Pin, security.isignercertificate_pin_property
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
 - ISignerCertificate.Pin
 - ISignerCertificate.put_Pin
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
- ISignerCertificate.put_Pin
: 
---

# ISignerCertificate::put_Pin


## -description


The <b>Pin</b> property specifies a personal identification number (PIN) used to  authenticate a smart card user. A user must be authenticated before accessing the private key container on the smart card.

This property is write-only.


## -parameters


## -remarks



Call this property to specify a value before calling the <a href="https://msdn.microsoft.com/en-us/library/Aa376832(v=VS.85).aspx">Initialize</a> method. The <b>Pin</b> property internally sets the pin number on the  <a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a> object. You can retrieve the private key object by calling <a href="https://msdn.microsoft.com/en-us/library/Aa376836(v=VS.85).aspx">PrivateKey</a>. You can call the following properties to retrieve additional information about the signing certificate object:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376831(v=VS.85).aspx">Certificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376834(v=VS.85).aspx">ParentWindow</a>
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
 

 

