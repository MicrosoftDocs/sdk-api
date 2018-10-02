---
UID: NF:wincrypt.CertCreateCRLContext
title: CertCreateCRLContext function
author: windows-sdk-content
description: The CertCreateCRLContext function creates a certificate revocation list (CRL) context from an encoded CRL. The created context is not persisted to a certificate store. It makes a copy of the encoded CRL within the created context.
old-location: security\certcreatecrlcontext.htm
tech.root: seccrypto
ms.assetid: 23d9dfb0-926d-443e-b960-a03338f1cc1b
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: CertCreateCRLContext, CertCreateCRLContext function [Security], _crypto2_certcreatecrlcontext, security.certcreatecrlcontext, wincrypt/CertCreateCRLContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertCreateCRLContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertCreateCRLContext function


## -description


The <b>CertCreateCRLContext</b> function creates a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a> from an encoded CRL. The created context is not persisted to a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a>. It makes a copy of the encoded CRL within the created context.


## -parameters




### -param dwCertEncodingType [in]

Specifies the type of encoding used. It is always acceptable to specify both the certificate and <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>



### -param pbCrlEncoded [in]

A pointer to a buffer containing the encoded <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">CRL</a> from which the context is to be created.


### -param cbCrlEncoded [in]

The size, in bytes, of the <i>pbCrlEncoded</i> buffer.


## -returns



If the function succeeds, the return value is a pointer to a read-only 
<a href="https://msdn.microsoft.com/cf7cabcd-b469-492a-b855-8870465ea1cc">CRL_CONTEXT</a>.

If the function fails and is unable to decode and create the <a href="https://msdn.microsoft.com/cf7cabcd-b469-492a-b855-8870465ea1cc">CRL_CONTEXT</a>, the return value is <b>NULL</b>. For extended error information, call 
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
Invalid certificate encoding type. Currently, only the encoding type X509_ASN_ENCODING is supported.

</td>
</tr>
</table>
 

If the function fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> may return an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="https://msdn.microsoft.com/cb1f34dd-dab4-4ffb-a73b-79a214290509">ASN.1 Encoding/Decoding Return Values</a>.




## -remarks



The 
<a href="https://msdn.microsoft.com/cf7cabcd-b469-492a-b855-8870465ea1cc">CRL_CONTEXT</a> must be freed by calling 
<a href="https://msdn.microsoft.com/19a590a5-bd39-4bbe-ad86-4e648baa1ba8">CertFreeCRLContext</a>. 
<a href="https://msdn.microsoft.com/ea14c494-d1c7-46d0-9d56-fc89a4b4afa9">CertDuplicateCRLContext</a> can be called to make a duplicate. 
<a href="https://msdn.microsoft.com/7e4a0a39-ce55-4171-9b66-31c1c28d895f">CertSetCRLContextProperty</a> and 
<a href="https://msdn.microsoft.com/16c2cc06-28fd-42d9-a377-0df2eaeeae56">CertGetCRLContextProperty</a> can be called to store and read properties for the CRL.




## -see-also




<a href="https://msdn.microsoft.com/cf7cabcd-b469-492a-b855-8870465ea1cc">CRL_CONTEXT</a>



<a href="https://msdn.microsoft.com/172c59ee-9e06-4169-aaa7-2624e3fcf015">CertCreateCTLContext</a>



<a href="https://msdn.microsoft.com/a32714c4-ee88-48a8-a40a-bbbfec0613ac">CertCreateCertificateContext</a>



<a href="https://msdn.microsoft.com/ea14c494-d1c7-46d0-9d56-fc89a4b4afa9">CertDuplicateCRLContext</a>



<a href="https://msdn.microsoft.com/19a590a5-bd39-4bbe-ad86-4e648baa1ba8">CertFreeCRLContext</a>



<a href="https://msdn.microsoft.com/16c2cc06-28fd-42d9-a377-0df2eaeeae56">CertGetCRLContextProperty</a>



<a href="https://msdn.microsoft.com/7e4a0a39-ce55-4171-9b66-31c1c28d895f">CertSetCRLContextProperty</a>



<a href="cryptography_functions.htm">Certificate Revocation List Functions</a>
 

 

