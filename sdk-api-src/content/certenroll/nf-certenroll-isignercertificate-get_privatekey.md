---
UID: NF:certenroll.ISignerCertificate.get_PrivateKey
title: ISignerCertificate::get_PrivateKey
author: windows-sdk-content
description: Retrieves the private key associated with the ISignerCertificate object.
old-location: security\isignercertificate_privatekey_property.htm
tech.root: SecCertEnroll
ms.assetid: 047a22ba-9817-45b7-aa9a-356245d2b824
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ISignerCertificate interface [Security],PrivateKey property, ISignerCertificate.PrivateKey, ISignerCertificate.get_PrivateKey, ISignerCertificate::PrivateKey, ISignerCertificate::get_PrivateKey, PrivateKey property [Security], PrivateKey property [Security],ISignerCertificate interface, certenroll/ISignerCertificate::PrivateKey, certenroll/ISignerCertificate::get_PrivateKey, get_PrivateKey, security.isignercertificate_privatekey_property
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
 - ISignerCertificate.PrivateKey
 - ISignerCertificate.get_PrivateKey
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
- ISignerCertificate.get_PrivateKey
: 
---

# ISignerCertificate::get_PrivateKey


## -description


The <b>PrivateKey</b> property retrieves the private key associated with the <a href="https://msdn.microsoft.com/en-us/library/Aa376820(v=VS.85).aspx">ISignerCertificate</a> object.

This property is read-only.


## -parameters


## -remarks



When you call the <a href="https://msdn.microsoft.com/en-us/library/Aa376832(v=VS.85).aspx">Initialize</a> method the Certificate Enrollment Control retrieves the signing certificate from the personal store and uses it to find an associated private key. You can also call the following properties to retrieve information about the signing certificate object:<ul>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa376839(v=VS.85).aspx">Silent</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376840(v=VS.85).aspx">UIContextMessage</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376820(v=VS.85).aspx">ISignerCertificate</a>
 

 

