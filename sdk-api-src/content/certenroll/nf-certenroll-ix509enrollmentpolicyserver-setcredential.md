---
UID: NF:certenroll.IX509EnrollmentPolicyServer.SetCredential
title: IX509EnrollmentPolicyServer::SetCredential (certenroll.h)
description: Sets the credential used to contact the certificate enrollment policy (CEP) server.
helpviewer_keywords: ["IX509EnrollmentPolicyServer interface [Security]","SetCredential method","IX509EnrollmentPolicyServer.SetCredential","IX509EnrollmentPolicyServer::SetCredential","SetCredential","SetCredential method [Security]","SetCredential method [Security]","IX509EnrollmentPolicyServer interface","X509AuthAnonymous","X509AuthCertificate","X509AuthKerberos","X509AuthUsername","certenroll/IX509EnrollmentPolicyServer::SetCredential","security.ix509enrollmentpolicyserver_setcredential"]
old-location: security\ix509enrollmentpolicyserver_setcredential.htm
tech.root: security
ms.assetid: 64ea6d9e-8eca-4a1b-95a0-ecc5c0d37df3
ms.date: 12/05/2018
ms.keywords: IX509EnrollmentPolicyServer interface [Security],SetCredential method, IX509EnrollmentPolicyServer.SetCredential, IX509EnrollmentPolicyServer::SetCredential, SetCredential, SetCredential method [Security], SetCredential method [Security],IX509EnrollmentPolicyServer interface, X509AuthAnonymous, X509AuthCertificate, X509AuthKerberos, X509AuthUsername, certenroll/IX509EnrollmentPolicyServer::SetCredential, security.ix509enrollmentpolicyserver_setcredential
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509EnrollmentPolicyServer::SetCredential
 - certenroll/IX509EnrollmentPolicyServer::SetCredential
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.h
api_name:
 - IX509EnrollmentPolicyServer.SetCredential
---

# IX509EnrollmentPolicyServer::SetCredential


## -description

The <b>SetCredential</b> method sets the credential used to contact the certificate enrollment policy (CEP) server.

## -parameters

### -param hWndParent [in]

Parent window handle.

### -param flag [in]

An <a href="/windows/desktop/api/certcli/ne-certcli-x509enrollmentauthflags">X509EnrollmentAuthFlags</a> enumeration value that specifies the authentication type. This can be one of the following values.

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
Anonymous authentication. Set the <i>strCredential</i> and <i>strPassword</i> parameters to <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="X509AuthKerberos"></a><a id="x509authkerberos"></a><a id="X509AUTHKERBEROS"></a><dl>
<dt><b>X509AuthKerberos</b></dt>
</dl>
</td>
<td width="60%">
Kerberos authentication. Set the <i>strCredential</i> and <i>strPassword</i> parameters to <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="X509AuthUsername"></a><a id="x509authusername"></a><a id="X509AUTHUSERNAME"></a><dl>
<dt><b>X509AuthUsername</b></dt>
</dl>
</td>
<td width="60%">
Clear text user name and password authentication. Set the <i>strCredential</i> and <i>strPassword</i> parameters to the user name and associated password. These strings are encrypted before transmission and are stored securely in the credential vault on the CEP server.

</td>
</tr>
<tr>
<td width="40%"><a id="X509AuthCertificate"></a><a id="x509authcertificate"></a><a id="X509AUTHCERTIFICATE"></a><dl>
<dt><b>X509AuthCertificate</b></dt>
</dl>
</td>
<td width="60%">
Client authentication certificate installed on the local computer and used by the server to verify the identity of the client. Set the <i>strPassword</i> parameter to <b>NULL</b> and set the certificate thumbprint, a 20-byte SHA1 hash of the certificate, in the <i>strCredential</i> parameter.

</td>
</tr>
</table>

### -param strCredential [in]

A <b>BSTR</b> variable that contains the credential.

### -param strPassword [in]

A <b>BSTR</b> variable that contains the password.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

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
The <i>flag</i> parameter is not a supported value.

</td>
</tr>
</table>

## -remarks

The <i>strCredential</i> and <i>strPassword</i> arguments will change depending on the value specified in the <i>flag</i> argument as shown in the following table.

<table>
<tr>
<th><i>flag</i> parameter </th>
<th><i>strCredential</i> parameter</th>
<th><i>strPassword</i> parameter</th>
</tr>
<tr>
<td>X509AuthAnonymous</td>
<td><b>NULL</b></td>
<td><b>NULL</b></td>
</tr>
<tr>
<td>X509AuthKerberos</td>
<td><b>NULL</b></td>
<td><b>NULL</b></td>
</tr>
<tr>
<td>X509AuthUsername</td>
<td>Clear text user name recognized by the CEP server.</td>
<td>Clear text password associated with the user name.</td>
</tr>
<tr>
<td>X509AuthCertificate</td>
<td>Contains a 20 byte SHA-1 hash (thumbprint) of the certificate.</td>
<td><b>NULL</b></td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentpolicyserver">IX509EnrollmentPolicyServer</a>