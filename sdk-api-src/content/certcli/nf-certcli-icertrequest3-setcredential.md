---
UID: NF:certcli.ICertRequest3.SetCredential
title: ICertRequest3::SetCredential
author: windows-sdk-content
description: Sets the credential used to contact the Certificate Enrollment Web Service.
old-location: security\icertrequest3_setcredential.htm
tech.root: seccrypto
ms.assetid: cdc3fc7b-aef6-4d73-876e-c958d7bf8f98
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: CCertRequest object [Security],SetCredential method, ICertRequest3 class [Security],SetCredential method, ICertRequest3.SetCredential, ICertRequest3::SetCredential, SetCredential, SetCredential method [Security], SetCredential method [Security],CCertRequest object, SetCredential method [Security],ICertRequest3 class, X509AuthAnonymous, X509AuthCertificate, X509AuthKerberos, X509AuthUsername, certcli/ICertRequest3::SetCredential, security.icertrequest3_setcredential
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certcli.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certidl.lib
req.dll: Certcli.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certcli.dll
api_name:
 - ICertRequest3.SetCredential
 - CCertRequest.SetCredential
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertRequest3::SetCredential


## -description


The <b>SetCredential</b> method sets the credential used to contact the Certificate Enrollment Web Service.


## -parameters




### -param hWnd [in]

A handle to the parent window.

You must set the <i>hWnd</i> parameter there is a UI presented to obtain the credential. 

For certificate based authorization, the handle is used if a UI prompt is needed to obtain the credential, for example, if the credential is on a smart card and a pin prompt is needed.

When using Kerberos, anonymous, or user name and password authentication, this parameter is ignored. 


### -param AuthType [in]

A value of the <a href="https://msdn.microsoft.com/84a7e6e3-dfbb-4c27-af63-e521103e1b00">X509EnrollmentAuthFlags</a> enumeration that specifies the authentication type.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="X509AuthAnonymous"></a><a id="x509authanonymous"></a><a id="X509AUTHANONYMOUS"></a><dl>
<dt><b>X509AuthAnonymous</b></dt>
</dl>
</td>
<td width="60%">
Anonymous authentication.

Set the <i>strCredential</i> and <i>strPassword</i> parameters to <b>NULL</b> or to empty strings.

</td>
</tr>
<tr>
<td width="40%"><a id="X509AuthCertificate"></a><a id="x509authcertificate"></a><a id="X509AUTHCERTIFICATE"></a><dl>
<dt><b>X509AuthCertificate</b></dt>
</dl>
</td>
<td width="60%">
Client authentication certificate installed on the local computer. The certificate contains a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> that is associated with a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> (not contained in the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate</a>). The certificate is used by the server to verify the identity of the client.

The <i>strCredential</i> parameter contains a binary 20-byte SHA-1 hash of the certificate to be passed to the Certificate Enrollment Web Service to authenticate the caller.  Set the <i>strPassword</i> parameter to <b>NULL</b> or an empty string.  The <i>strCredential</i> parameter must refer to a certificate installed in the relevant  personal certificate store, and it must have an associated private key that is accessible to the caller.

</td>
</tr>
<tr>
<td width="40%"><a id="X509AuthKerberos"></a><a id="x509authkerberos"></a><a id="X509AUTHKERBEROS"></a><dl>
<dt><b>X509AuthKerberos</b></dt>
</dl>
</td>
<td width="60%">
Kerberos authentication.

Set the <i>strCredential</i> and <i>strPassword</i> parameters to <b>NULL</b> or to empty strings.

</td>
</tr>
<tr>
<td width="40%"><a id="X509AuthUsername"></a><a id="x509authusername"></a><a id="X509AUTHUSERNAME"></a><dl>
<dt><b>X509AuthUsername</b></dt>
</dl>
</td>
<td width="60%">
Plaintext user name and password authentication. The user name and password are encrypted when they are stored in the credential vault on the client.

The <i>strCredential</i> and <i>strPassword</i> parameters contain a user name string and a plaintext password that are supported by the Certificate Enrollment Web Service to authenticate the caller.  Because an enrollment service connection always uses <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Secure Sockets Layer protocol</a> (SSL), the password is encrypted when sent over the wire.

</td>
</tr>
</table>
 


### -param strCredential [in]

A string that contains the credential.


### -param strPassword [in]

A string that contains the password.


## -returns



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
The <i>AuthType</i> parameter must be <b>X509AuthKerberos</b>.

</td>
</tr>
</table>
 




## -remarks



The <b>SetCredential</b> method must be called prior to calling the <a href="https://msdn.microsoft.com/22ae8d39-3f16-4f7d-94a0-aa68b03aaa0b">ICertRequest2::Submit</a> method.

The <i>strCredential</i> and <i>strPassword</i> arguments change depending on the value specified in the <i>AuthType</i> parameter as shown in the following table.

<table>
<tr>
<th><i>AuthType</i> parameter </th>
<th><i>strCredential</i> parameter</th>
<th><i>strPassword</i> parameter</th>
</tr>
<tr>
<td>
X509AuthAnonymous

</td>
<td>
<b>NULL</b>

</td>
<td>
<b>NULL</b>

</td>
</tr>
<tr>
<td>
X509AuthCertificate

</td>
<td>
A 20 byte SHA-1 hash (thumbprint) of the certificate

</td>
<td>
<b>NULL</b>

</td>
</tr>
<tr>
<td>
X509AuthKerberos

</td>
<td>
<b>NULL</b>

</td>
<td>
<b>NULL</b>

</td>
</tr>
<tr>
<td>
X509AuthUsername

</td>
<td>
A plaintext user name that is recognized by the Certificate Enrollment Web Service

</td>
<td>
A plaintext password that is associated with the user name

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/2f371aa6-492e-41ba-8455-66e9d5f5da44">CCertRequest</a>



<a href="https://msdn.microsoft.com/01de2ac0-4844-41a6-acef-e3e83b350393">ICertRequest3</a>
 

 

