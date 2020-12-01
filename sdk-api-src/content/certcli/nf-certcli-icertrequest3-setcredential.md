---
UID: NF:certcli.ICertRequest3.SetCredential
title: ICertRequest3::SetCredential (certcli.h)
description: Sets the credential used to contact the Certificate Enrollment Web Service.
helpviewer_keywords: ["CCertRequest object [Security]","SetCredential method","ICertRequest3 class [Security]","SetCredential method","ICertRequest3.SetCredential","ICertRequest3::SetCredential","SetCredential","SetCredential method [Security]","SetCredential method [Security]","CCertRequest object","SetCredential method [Security]","ICertRequest3 class","X509AuthAnonymous","X509AuthCertificate","X509AuthKerberos","X509AuthUsername","certcli/ICertRequest3::SetCredential","security.icertrequest3_setcredential"]
old-location: security\icertrequest3_setcredential.htm
tech.root: security
ms.assetid: cdc3fc7b-aef6-4d73-876e-c958d7bf8f98
ms.date: 12/05/2018
ms.keywords: CCertRequest object [Security],SetCredential method, ICertRequest3 class [Security],SetCredential method, ICertRequest3.SetCredential, ICertRequest3::SetCredential, SetCredential, SetCredential method [Security], SetCredential method [Security],CCertRequest object, SetCredential method [Security],ICertRequest3 class, X509AuthAnonymous, X509AuthCertificate, X509AuthKerberos, X509AuthUsername, certcli/ICertRequest3::SetCredential, security.icertrequest3_setcredential
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertRequest3::SetCredential
 - certcli/ICertRequest3::SetCredential
dev_langs:
 - c++
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

A value of the <a href="/windows/desktop/api/certcli/ne-certcli-x509enrollmentauthflags">X509EnrollmentAuthFlags</a> enumeration that specifies the authentication type.

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
Client authentication certificate installed on the local computer. The certificate contains a <a href="/windows/desktop/SecGloss/p-gly">public key</a> that is associated with a <a href="/windows/desktop/SecGloss/p-gly">private key</a> (not contained in the <a href="/windows/desktop/SecGloss/c-gly">certificate</a>). The certificate is used by the server to verify the identity of the client.

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

The <i>strCredential</i> and <i>strPassword</i> parameters contain a user name string and a plaintext password that are supported by the Certificate Enrollment Web Service to authenticate the caller.  Because an enrollment service connection always uses <a href="/windows/desktop/SecGloss/s-gly">Secure Sockets Layer protocol</a> (SSL), the password is encrypted when sent over the wire.

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

The <b>SetCredential</b> method must be called prior to calling the <a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-submit">ICertRequest2::Submit</a> method.

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

<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest">CCertRequest</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest3">ICertRequest3</a>