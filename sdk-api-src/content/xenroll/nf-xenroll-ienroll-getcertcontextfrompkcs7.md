---
UID: NF:xenroll.IEnroll.getCertContextFromPKCS7
title: IEnroll::getCertContextFromPKCS7
author: windows-sdk-content
description: Retrieves a certificate context based on a PKCS #7 message that was issued in response to a PKCS #10 certificate request.
old-location: security\ienroll4_getcertcontextfrompkcs7.htm
tech.root: seccrypto
ms.assetid: 3781729d-8b08-41b5-8ff4-1de19fc4ee2e
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: IEnroll interface [Security],getCertContextFromPKCS7 method, IEnroll.getCertContextFromPKCS7, IEnroll2 interface [Security],getCertContextFromPKCS7 method, IEnroll2::getCertContextFromPKCS7, IEnroll::getCertContextFromPKCS7, getCertContextFromPKCS7, getCertContextFromPKCS7 method [Security], getCertContextFromPKCS7 method [Security],IEnroll interface, getCertContextFromPKCS7 method [Security],IEnroll2 interface, security.ienroll4_getcertcontextfrompkcs7, xenroll/IEnroll2::getCertContextFromPKCS7, xenroll/IEnroll::getCertContextFromPKCS7
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
 - IEnroll.getCertContextFromPKCS7
 - IEnroll2.getCertContextFromPKCS7
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll::getCertContextFromPKCS7


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>getCertContextFromPKCS7</b> method retrieves a  certificate context based on a  PKCS #7 message that was  issued in response to a PKCS #10 certificate request.

This method retrieves the context for the single certificate that was issued even though a PKCS #7 message may contain many certificates specifying the certification chain of authority that issued the certificate.

This method was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.


## -parameters




### -param pBlobPKCS7 [in]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that represents the PKCS #7.


## -returns



The return value is a pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> representing the certificate context, or <b>NULL</b> if the method fails.




## -see-also




<a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a>



<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll2</a>
 

 

