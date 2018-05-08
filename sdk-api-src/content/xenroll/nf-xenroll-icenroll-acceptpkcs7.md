---
UID: NF:xenroll.ICEnroll.acceptPKCS7
title: ICEnroll::acceptPKCS7
author: windows-driver-content
description: Accepts and processes a PKCS #7 message that contains a certificate. The PKCS #7 is input as a parameter. This method was first defined in the ICEnroll interface.
old-location: security\icenroll4_acceptpkcs7.htm
old-project: SecCrypto
ms.assetid: 5a428d83-c846-4f44-a682-58c3e025c353
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: CEnroll object [Security],acceptPKCS7 method, ICEnroll interface [Security],acceptPKCS7 method, ICEnroll.acceptPKCS7, ICEnroll2 interface [Security],acceptPKCS7 method, ICEnroll2::acceptPKCS7, ICEnroll3 interface [Security],acceptPKCS7 method, ICEnroll3::acceptPKCS7, ICEnroll4 interface [Security],acceptPKCS7 method, ICEnroll4::acceptPKCS7, ICEnroll::acceptPKCS7, acceptPKCS7, acceptPKCS7 method [Security], acceptPKCS7 method [Security],CEnroll object, acceptPKCS7 method [Security],ICEnroll interface, acceptPKCS7 method [Security],ICEnroll2 interface, acceptPKCS7 method [Security],ICEnroll3 interface, acceptPKCS7 method [Security],ICEnroll4 interface, security.icenroll4_acceptpkcs7, xenroll/ICEnroll2::acceptPKCS7, xenroll/ICEnroll3::acceptPKCS7, xenroll/ICEnroll4::acceptPKCS7, xenroll/ICEnroll::acceptPKCS7
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
req.typenames: XBL_IDP_AUTH_TOKEN_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Xenroll.dll
api_name:
-	ICEnroll4.acceptPKCS7
-	ICEnroll3.acceptPKCS7
-	ICEnroll2.acceptPKCS7
-	ICEnroll.acceptPKCS7
-	CEnroll.acceptPKCS7
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# ICEnroll::acceptPKCS7


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>acceptPKCS7</b> method accepts and processes a PKCS #7 message that contains a certificate. The PKCS #7 is input as a parameter. This method was first defined in the <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a> interface.


## -parameters




### -param PKCS7 [in]

Represents the base64-encoded PKCS #7 that contains the certificate and the chain of certificates that identifies the issuer.


## -returns



<h3>VB</h3>

						 The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Upon successful completion of this function, the PKCS #7 will be accepted.




## -remarks



The PKCS #7 input as a parameter for <b>acceptPKCS7</b> contains the request certificate and the chain of certificates identifying the issuer of the certificate. Typically, but not always, the chain of certificates does not include the root. The PKCS #7 can be in base64-encoded, binary, or <a href="https://msdn.microsoft.com/28dba6ef-939f-4789-9789-ee6e0fef0177">X.509</a> certificate format (with or without the begin cert / end cert tags). The certificate and the associated keys generated for it are put in the MY store. A <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">root certificate</a> is placed in the ROOT store and the rest of the chain of certificates are placed in the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) store. If any ROOT certificates found in the PKCS #7 are accepted, Crypt32 will notify the user that a ROOT certificate is being added to his store. The user has the option of declining the ROOT certificate. This option is provided so that the user can decline to place an untrusted root in the ROOT store. Declining to place the ROOT in the ROOT store will not cause Certificate Enrollment Control to fail acceptance.


By default, the system stores MY, CA, ROOT, and REQUEST are used to store the certificates. However, you can specify other stores by assigning the following properties before calling this method:

<ul>
<li>
<a href="https://msdn.microsoft.com/aa08e88d-bd1f-4bd6-806e-56f720846623">MyStoreName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/29616175-7195-430e-a85b-99b50e276e7f">CAStoreName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5b686ade-e8ee-4c59-ab90-05088f575acd">RootStoreName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c42d1dc8-ee1c-4bb7-b54f-6ede3301ce03">RequestStoreName</a>
</li>
</ul>


When this method is called from script, the method displays a user interface that asks whether the user will allow installation of a  certificate.




## -see-also




<a href="https://msdn.microsoft.com/29616175-7195-430e-a85b-99b50e276e7f">CAStoreName</a>



<a href="https://msdn.microsoft.com/7f13549d-811b-496b-abdd-7e52cbc2ed54">CEnroll</a>



<a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>



<a href="https://msdn.microsoft.com/12c51daf-a72f-43da-9fb7-20ec261b4917">ICEnroll2</a>



<a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>



<a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a>



<a href="https://msdn.microsoft.com/aa08e88d-bd1f-4bd6-806e-56f720846623">MyStoreName</a>



<a href="https://msdn.microsoft.com/c42d1dc8-ee1c-4bb7-b54f-6ede3301ce03">RequestStoreName</a>



<a href="https://msdn.microsoft.com/5b686ade-e8ee-4c59-ab90-05088f575acd">RootStoreName</a>



<a href="https://msdn.microsoft.com/dae9f6b8-6690-47cc-9397-168c1ff54c55">acceptFilePKCS7</a>
 

 

