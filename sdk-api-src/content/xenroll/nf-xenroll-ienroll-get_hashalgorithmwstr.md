---
UID: NF:xenroll.IEnroll.get_HashAlgorithmWStr
title: IEnroll::get_HashAlgorithmWStr
author: windows-sdk-content
description: Sets or retrieves only the signature hashing algorithm used to sign the PKCS #10 certification request.
old-location: security\ienroll4_hashalgorithmwstr.htm
tech.root: seccrypto
ms.assetid: c359c4c8-f53d-48f1-a2ac-9275751b48dc
ms.author: windowssdkdev
ms.date: 12/04/2018
ms.keywords: HashAlgorithmWStr property [Security], HashAlgorithmWStr property [Security],IEnroll interface, IEnroll interface [Security],HashAlgorithmWStr property, IEnroll.HashAlgorithmWStr, IEnroll.get_HashAlgorithmWStr, IEnroll::HashAlgorithmWStr, IEnroll::get_HashAlgorithmWStr, IEnroll::put_HashAlgorithmWStr, get_HashAlgorithmWStr, security.ienroll4_hashalgorithmwstr, xenroll/IEnroll::HashAlgorithmWStr, xenroll/IEnroll::get_HashAlgorithmWStr, xenroll/IEnroll::put_HashAlgorithmWStr
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
 - IEnroll.HashAlgorithmWStr
 - IEnroll.get_HashAlgorithmWStr
 - IEnroll.put_HashAlgorithmWStr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll::get_HashAlgorithmWStr


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>HashAlgorithmWStr</b> property  sets or retrieves only   the signature <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hashing algorithm</a> used to sign the PKCS #10 certification request.

This property was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks



This  signature hashing algorithm is not to be confused with the hashing algorithm used to sign the certificate. The enrollment control currently supports any OID for hashing algorithms, plus the following display name values: SHA1 (the default), MD2, and MD5. When retrieving this property, the retrieved value is in OID format (that is, SHA1 appears as 1.3.14.3.2.29). When setting this property, the corresponding OID format can be used as an alternative to the text shown for the defined friendly values.

The Certificate Enrollment Control considers the value of the <b>HashAlgorithmWStr</b> property  as a hint to the hashing algorithm to use for signing the PKCS #10 certification request. If the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) supports the algorithm specified in the <b>HashAlgorithmWStr</b> property, the algorithm will be used. Otherwise, the Certificate Enrollment Control will try to use SHA1. If SHA1 is not supported by the CSP, then MD5 will be tried. If neither SHA1 nor MD5 is supported, the Certificate Enrollment Control will try to use the first hashing algorithm returned from the CSP.


The <b>HashAlgorithmWStr</b>  property affects the behavior of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/ebbcc9ad-9f87-4abe-963b-38c57a60e45e">createPKCS10WStr</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5edd54c5-9dfb-44b8-a293-4fe6a8de45e3">createFilePKCS10WStr</a>
</li>
</ul>


If both the 
<a href="https://msdn.microsoft.com/ebf4a7c7-4bd4-4a5f-8f32-bb30a6a8af0e">HashAlgID</a> and <b>HashAlgorithmWStr</b> properties are set, whichever is last updated will specify which hashing algorithm will be used to sign the PKCS #10 certification request.




## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll</a>
 

 

