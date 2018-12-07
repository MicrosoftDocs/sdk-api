---
UID: NF:certenroll.ISignerCertificate.put_ParentWindow
title: ISignerCertificate::put_ParentWindow
author: windows-sdk-content
description: Specifies or retrieves the ID of the window used to display signing certificate information.
old-location: security\isignercertificate_parentwindow_property.htm
tech.root: seccertenroll
ms.assetid: a1749c92-11e4-4726-a355-ccdd245b4df8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISignerCertificate interface [Security],ParentWindow property, ISignerCertificate.ParentWindow, ISignerCertificate.put_ParentWindow, ISignerCertificate::ParentWindow, ISignerCertificate::get_ParentWindow, ISignerCertificate::put_ParentWindow, ParentWindow property [Security], ParentWindow property [Security],ISignerCertificate interface, certenroll/ISignerCertificate::ParentWindow, certenroll/ISignerCertificate::get_ParentWindow, certenroll/ISignerCertificate::put_ParentWindow, put_ParentWindow, security.isignercertificate_parentwindow_property
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
 - ISignerCertificate.ParentWindow
 - ISignerCertificate.get_ParentWindow
 - ISignerCertificate.put_ParentWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISignerCertificate::put_ParentWindow


## -description


The <b>ParentWindow</b> property specifies or retrieves the ID of the window used to display signing certificate information.

This property is read/write.


## -parameters


## -remarks



Call this property to specify a window ID before calling the <a href="https://msdn.microsoft.com/en-us/library/Aa376832(v=VS.85).aspx">Initialize</a> method. The <b>ParentWindow</b> property internally sets the window ID on the  <a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a> object. You can retrieve the private key object by calling the <a href="https://msdn.microsoft.com/en-us/library/Aa376836(v=VS.85).aspx">PrivateKey</a> property. You can call the following properties to retrieve additional information about the signing certificate object:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376831(v=VS.85).aspx">Certificate</a>
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
 

 

