---
UID: NF:certenroll.ISignerCertificate.get_UIContextMessage
title: ISignerCertificate::get_UIContextMessage
author: windows-sdk-content
description: Specifies or retrieves a string that contains user interface text associated with the signing certificate.
old-location: security\isignercertificate_uicontextmessage_property.htm
tech.root: SecCertEnroll
ms.assetid: 0fd874b0-9093-4c1b-94a0-a2aaad19010e
ms.author: windowssdkdev
ms.date: 08/29/2018
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
---

# ISignerCertificate::get_UIContextMessage


## -description


The <b>UIContextMessage</b> property specifies or retrieves a string that contains user interface text associated with the  signing certificate.

This property is read/write.


## -parameters


## -remarks



Call this property to specify a value before calling the <a href="https://msdn.microsoft.com/en-us/library/Aa376832(v=VS.85).aspx">Initialize</a> method. You can also call the following properties to retrieve additional information about the signing certificate object:

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
<a href="https://msdn.microsoft.com/en-us/library/Aa376836(v=VS.85).aspx">PrivateKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376838(v=VS.85).aspx">SignatureInformation</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376839(v=VS.85).aspx">Silent</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376820(v=VS.85).aspx">ISignerCertificate</a>
 

 

