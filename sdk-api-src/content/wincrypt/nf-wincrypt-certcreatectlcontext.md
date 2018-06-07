---
UID: NF:wincrypt.CertCreateCTLContext
title: CertCreateCTLContext function
author: windows-sdk-content
description: The CertCreateCTLContext function creates a certificate trust list (CTL) context from an encoded CTL. The created context is not persisted to a certificate store. The function makes a copy of the encoded CTL within the created context.
old-location: security\certcreatectlcontext.htm
old-project: SecCrypto
ms.assetid: 172c59ee-9e06-4169-aaa7-2624e3fcf015
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: CertCreateCTLContext, CertCreateCTLContext function [Security], _crypto2_certcreatectlcontext, security.certcreatectlcontext, wincrypt/CertCreateCTLContext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
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
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertCreateCTLContext
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertCreateCTLContext function


## -description



			The <b>CertCreateCTLContext</b> function creates a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust list</a> (CTL) context from an encoded CTL. The created context is not persisted to a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a>. The function makes a copy of the encoded CTL within the created context.


## -parameters




### -param dwMsgAndCertEncodingType [in]

Specifies the type of encoding used. Both the certificate and <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding types</a> must be specified by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>



### -param pbCtlEncoded [in]

A pointer to a buffer containing the encoded CTL from which the context is to be created.


### -param cbCtlEncoded [in]

The size, in bytes, of the <i>pbCtlEncoded</i> buffer.


## -returns




						If the function succeeds, the return value is a pointer to a read-only 
<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a>.

If the function fails and is unable to decode and create the <a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a>, the return value is <b>NULL</b>. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following table shows a possible error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid certificate encoding type. Only PKCS_7_ASN_ENCODING and X509_ASN_ENCODING are supported.

</td>
</tr>
</table>
 

If the function fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> may return an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="https://msdn.microsoft.com/cb1f34dd-dab4-4ffb-a73b-79a214290509">ASN.1 Encoding/Decoding Return Values</a>.




## -remarks



The 
<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a> must be freed by calling 
<a href="https://msdn.microsoft.com/84b1aa0c-44d9-4a2f-861c-fa7d8caac192">CertFreeCTLContext</a>. 
<a href="https://msdn.microsoft.com/512d246f-9f22-4ac1-a4fc-d5c615a65cf9">CertDuplicateCTLContext</a> can be called to make a duplicate. 
<a href="https://msdn.microsoft.com/3af01ca6-6fa1-4510-872a-b5e13e07f49f">CertSetCTLContextProperty</a> and 
<a href="https://msdn.microsoft.com/16e45fe1-2710-4fa1-82da-c298645d7379">CertGetCTLContextProperty</a> can be called to store and read properties for the CTL.




## -see-also




<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a>



<a href="https://msdn.microsoft.com/23d9dfb0-926d-443e-b960-a03338f1cc1b">CertCreateCRLContext</a>



<a href="https://msdn.microsoft.com/a32714c4-ee88-48a8-a40a-bbbfec0613ac">CertCreateCertificateContext</a>



<a href="https://msdn.microsoft.com/512d246f-9f22-4ac1-a4fc-d5c615a65cf9">CertDuplicateCTLContext</a>



<a href="https://msdn.microsoft.com/84b1aa0c-44d9-4a2f-861c-fa7d8caac192">CertFreeCTLContext</a>



<a href="https://msdn.microsoft.com/16e45fe1-2710-4fa1-82da-c298645d7379">CertGetCTLContextProperty</a>



<a href="https://msdn.microsoft.com/3af01ca6-6fa1-4510-872a-b5e13e07f49f">CertSetCTLContextProperty</a>



<a href="https://www.bing.com/search?q=Certificate+Trust+List+Functions">Certificate Trust List Functions</a>
 

 

