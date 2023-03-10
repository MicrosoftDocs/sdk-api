---
UID: NF:certenroll.IX509EnrollmentHelper.AddPolicyServer
title: IX509EnrollmentHelper::AddPolicyServer (certenroll.h)
description: Registers a certificate enrollment policy (CEP) server and saves CEP access credentials in the credential cache.
helpviewer_keywords: ["AddPolicyServer","AddPolicyServer method [Security]","AddPolicyServer method [Security]","IX509EnrollmentHelper interface","IX509EnrollmentHelper interface [Security]","AddPolicyServer method","IX509EnrollmentHelper.AddPolicyServer","IX509EnrollmentHelper::AddPolicyServer","PsfAllowUnTrustedCA","PsfAutoEnrollmentEnabled","X509AuthAnonymous","X509AuthCertificate","X509AuthKerberos","X509AuthUsername","certenroll/IX509EnrollmentHelper::AddPolicyServer","security.ix509enrollmenthelper_addpolicyserver"]
old-location: security\ix509enrollmenthelper_addpolicyserver.htm
tech.root: security
ms.assetid: 6b341b5a-88f2-4221-812d-b2997829aa4c
ms.date: 12/05/2018
ms.keywords: AddPolicyServer, AddPolicyServer method [Security], AddPolicyServer method [Security],IX509EnrollmentHelper interface, IX509EnrollmentHelper interface [Security],AddPolicyServer method, IX509EnrollmentHelper.AddPolicyServer, IX509EnrollmentHelper::AddPolicyServer, PsfAllowUnTrustedCA, PsfAutoEnrollmentEnabled, X509AuthAnonymous, X509AuthCertificate, X509AuthKerberos, X509AuthUsername, certenroll/IX509EnrollmentHelper::AddPolicyServer, security.ix509enrollmenthelper_addpolicyserver
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
 - IX509EnrollmentHelper::AddPolicyServer
 - certenroll/IX509EnrollmentHelper::AddPolicyServer
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
 - IX509EnrollmentHelper.AddPolicyServer
---

# IX509EnrollmentHelper::AddPolicyServer


## -description

The <b>AddPolicyServer</b> method registers a certificate enrollment policy (CEP) server and saves CEP access credentials in the credential cache. This method is web enabled.

## -parameters

### -param strEnrollmentPolicyServerURI [in]

A <b>BSTR</b> that contains the certificate enrollment policy server URL.

### -param strEnrollmentPolicyID [in]

A <b>BSTR</b> that contains the certificate enrollment policy server ID. The ID can be any string. It is set by the administrator who installs the CEP server.

### -param EnrollmentPolicyServerFlags [in]

A <a href="/windows/desktop/api/certenroll/ne-certenroll-policyserverurlflags">PolicyServerUrlFlags</a> enumeration value. For the <b>AddPolicyServer</b> function, you can specify a bitwise <b>OR</b> of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PsfAutoEnrollmentEnabled"></a><a id="psfautoenrollmentenabled"></a><a id="PSFAUTOENROLLMENTENABLED"></a><dl>
<dt><b>PsfAutoEnrollmentEnabled</b></dt>
</dl>
</td>
<td width="60%">
Automatic certificate enrollment is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="PsfAllowUnTrustedCA"></a><a id="psfallowuntrustedca"></a><a id="PSFALLOWUNTRUSTEDCA"></a><dl>
<dt><b>PsfAllowUnTrustedCA</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the certificate of the issuing CA need not be trusted by the client to install a certificate signed by the CA.

</td>
</tr>
</table>

### -param authFlags [in]

An <a href="/windows/desktop/api/certcli/ne-certcli-x509enrollmentauthflags">X509EnrollmentAuthFlags</a> enumeration value that specifies the client authentication type.  This can be one of the following values.

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

A <b>BSTR</b> that contains the credential.

### -param strPassword [in]

A <b>BSTR</b> that contains a clear text password.

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
The <i>strEnrollmentPolicyServerURI</i>,  <i>strCredential</i>, or <i>strPassword</i> parameters cannot be <b>NULL</b> or empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ARITHMETIC_OVERFLOW)</b></dt>
</dl>
</td>
<td width="60%">
The <i>strPassword</i>, <i>strCredential</i>, or <i>strEnrollmentServerURI</i> parameters exceed 64,000 characters or contain embedded null characters.

</td>
</tr>
</table>

## -remarks

The <i>strCredential</i> and <i>strPassword</i> arguments change depending on the value specified in the <i>authFlags</i> argument as shown in the following table.

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

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmenthelper">IX509EnrollmentHelper</a>