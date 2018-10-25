---
UID: NF:xenroll.IEnroll.get_WriteCertToCSP
title: IEnroll::get_WriteCertToCSP
author: windows-sdk-content
description: Sets or retrieves a Boolean value that determines whether a certificate should be written to the cryptographic service provider (CSP).
old-location: security\ienroll4_writecerttocsp.htm
tech.root: seccrypto
ms.assetid: 07463f0d-f46c-4bc3-8170-0a480b826049
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: IEnroll interface [Security],WriteCertToCSP property, IEnroll.WriteCertToCSP, IEnroll.get_WriteCertToCSP, IEnroll::WriteCertToCSP, IEnroll::get_WriteCertToCSP, IEnroll::put_WriteCertToCSP, WriteCertToCSP property [Security], WriteCertToCSP property [Security],IEnroll interface, get_WriteCertToCSP, security.ienroll4_writecerttocsp, xenroll/IEnroll::WriteCertToCSP, xenroll/IEnroll::get_WriteCertToCSP, xenroll/IEnroll::put_WriteCertToCSP
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll.WriteCertToCSP
 - IEnroll.get_WriteCertToCSP
 - IEnroll.put_WriteCertToCSP
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll::get_WriteCertToCSP


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WriteCertToCSP</b> property sets or retrieves a Boolean value that determines whether a certificate should be written to the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP).

This property was first defined by the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks



This property is typically used with smart cards, where the certificate is written to the smart card in addition to being written to the "MY" store.

The default value is <b>true</b>, which means that the Certificate Enrollment Control will try to write the certificate to the CSP but will not fail unless a hardware token error is encountered. If this value is <b>true</b>, but no smart card or other hardware-dependent CSP is installed, then hardware token errors will be ignored.

To explicitly force that the Certificate Enrollment Control not attempt to write to the CSP, set this value to false.


<b>WriteCertToCSP</b> affects the behavior of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/8772f528-2c33-48f4-bb0c-cfde91cf2fba">acceptPKCS7Blob</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9c2b99df-769b-457b-b5c5-7690b73d6f84">acceptFilePKCS7WStr</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll</a>
 

 

