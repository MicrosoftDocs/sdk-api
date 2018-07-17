---
UID: NF:xenroll.IEnroll.acceptFilePKCS7WStr
title: IEnroll::acceptFilePKCS7WStr
author: windows-sdk-content
description: Accepts and processes a PKCS #7 message containing a certificate, then stores the message to a file.
old-location: security\ienroll4_acceptfilepkcs7wstr.htm
old-project: SecCrypto
ms.assetid: 9c2b99df-769b-457b-b5c5-7690b73d6f84
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IEnroll interface [Security],acceptFilePKCS7WStr method, IEnroll.acceptFilePKCS7WStr, IEnroll::acceptFilePKCS7WStr, acceptFilePKCS7WStr, acceptFilePKCS7WStr method [Security], acceptFilePKCS7WStr method [Security],IEnroll interface, security.ienroll4_acceptfilepkcs7wstr, xenroll/IEnroll::acceptFilePKCS7WStr
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: XBL_IDP_AUTH_TOKEN_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll.acceptFilePKCS7WStr
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IEnroll::acceptFilePKCS7WStr


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>acceptFilePKCS7WStr</b> method  accepts and processes a PKCS #7 message containing a certificate, then stores the message to a file. This method was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.


## -parameters




### -param wszPKCS7FileName [in]

Specifies the name of the file containing the PKCS #7.


## -returns




						 The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Upon successful completion of this function, the PKCS #7 in the file will be accepted.




## -remarks




By default, the MY, CA, ROOT, and REQUEST system stores are used to store the certificates. However, you can specify other stores by assigning the following properties before calling this method:

<ul>
<li>
<a href="https://msdn.microsoft.com/077bc593-0071-4f41-8d07-141c9959b6ed">MyStoreNameWStr</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4c016649-a780-45c1-94a4-fb08c15c4e0f">CAStoreNameWStr</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d1b60ba4-974e-43d4-a8f9-8ca619d6b878">RootStoreNameWStr</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4ad739c0-fcf7-435b-b427-96ecca1afab7">RequestStoreNameWStr</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll</a>
 

 

