---
UID: NF:xenroll.IEnroll.acceptPKCS7Blob
title: IEnroll::acceptPKCS7Blob
author: windows-sdk-content
description: Accepts and processes a PKCS #7 message containing a certificate. The PKCS #7 is input as a parameter.
old-location: security\ienroll4_acceptpkcs7blob.htm
tech.root: seccrypto
ms.assetid: 8772f528-2c33-48f4-bb0c-cfde91cf2fba
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnroll interface [Security],acceptPKCS7Blob method, IEnroll.acceptPKCS7Blob, IEnroll::acceptPKCS7Blob, acceptPKCS7Blob, acceptPKCS7Blob method [Security], acceptPKCS7Blob method [Security],IEnroll interface, security.ienroll4_acceptpkcs7blob, xenroll/IEnroll::acceptPKCS7Blob
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
 - IEnroll.acceptPKCS7Blob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll::acceptPKCS7Blob


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>acceptPKCS7Blob</b> method accepts and processes a PKCS #7 message containing a certificate. The PKCS #7 is input as a parameter. This method was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.


## -parameters




### -param pBlobPKCS7 [in]

Represents the base64-encoded PKCS #7 containing the certificate and the chain of certificates identifying the issuer.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Upon successful completion of this function, the PKCS #7 will be accepted.




## -remarks



The PKCS #7 input as a parameter for <b>acceptPKCS7Blob</b> contains the request certificate and the chain of certificates identifying the issuer of the certificate. Typically, but not always, the chain of certificates does not include the root. The PKCS #7 can be in base64-encoded, binary, or <a href="https://msdn.microsoft.com/28dba6ef-939f-4789-9789-ee6e0fef0177">X.509</a> certificate format (with or without the "begin cert"  and  "end cert" tags). The certificate and the associated keys generated for it are put in the MY store. A <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">root certificate</a> is placed in the ROOT store, and the rest of the chain of certificates is placed in the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) store. If any ROOT certificates found in the PKCS #7 are accepted, Crypt32 will notify the user that a ROOT certificate is being added to the user's store. The user has the option of declining the ROOT certificate. This option is provided so that the user can decline to place an untrusted root in the ROOT store. Declining to place the ROOT in the ROOT store will not cause Certificate Enrollment Control to fail acceptance.


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
 

 

