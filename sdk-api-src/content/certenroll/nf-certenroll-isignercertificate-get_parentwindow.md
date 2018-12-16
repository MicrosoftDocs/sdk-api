---
UID: NF:certenroll.ISignerCertificate.get_ParentWindow
title: ISignerCertificate::get_ParentWindow
author: windows-sdk-content
description: Specifies or retrieves the ID of the window used to display signing certificate information.
old-location: security\isignercertificate_parentwindow_property.htm
tech.root: seccertenroll
ms.assetid: a1749c92-11e4-4726-a355-ccdd245b4df8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISignerCertificate interface [Security],ParentWindow property, ISignerCertificate.ParentWindow, ISignerCertificate.get_ParentWindow, ISignerCertificate::ParentWindow, ISignerCertificate::get_ParentWindow, ISignerCertificate::put_ParentWindow, ParentWindow property [Security], ParentWindow property [Security],ISignerCertificate interface, certenroll/ISignerCertificate::ParentWindow, certenroll/ISignerCertificate::get_ParentWindow, certenroll/ISignerCertificate::put_ParentWindow, get_ParentWindow, security.isignercertificate_parentwindow_property
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

# ISignerCertificate::get_ParentWindow


## -description


The <b>ParentWindow</b> property specifies or retrieves the ID of the window used to display signing certificate information.

This property is read/write.


## -parameters


## -remarks



Call this property to specify a window ID before calling the <a href="https://msdn.microsoft.com/2553f0bc-a177-49fc-932f-080cb4bd7a5c">Initialize</a> method. The <b>ParentWindow</b> property internally sets the window ID on the  <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> object. You can retrieve the private key object by calling the <a href="https://msdn.microsoft.com/047a22ba-9817-45b7-aa9a-356245d2b824">PrivateKey</a> property. You can call the following properties to retrieve additional information about the signing certificate object:<ul>
<li>
<a href="https://msdn.microsoft.com/7c7cc326-593d-4b2b-b8db-46aaf894279b">Certificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/695d895e-0646-4a2e-a699-86674f919bad">Pin</a>
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
 

 

