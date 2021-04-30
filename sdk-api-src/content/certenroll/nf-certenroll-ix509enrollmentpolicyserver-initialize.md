---
UID: NF:certenroll.IX509EnrollmentPolicyServer.Initialize
title: IX509EnrollmentPolicyServer::Initialize (certenroll.h)
description: Initializes an IX509EnrollmentPolicyServer object.
helpviewer_keywords: ["ContextAdministratorForceMachine","ContextMachine","ContextUser","IX509EnrollmentPolicyServer interface [Security]","Initialize method","IX509EnrollmentPolicyServer.Initialize","IX509EnrollmentPolicyServer::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","IX509EnrollmentPolicyServer interface","X509AuthAnonymous","X509AuthCertificate","X509AuthKerberos","X509AuthUsername","certenroll/IX509EnrollmentPolicyServer::Initialize","security.ix509enrollmentpolicyserver_initialize"]
old-location: security\ix509enrollmentpolicyserver_initialize.htm
tech.root: security
ms.assetid: b0d848a2-1bac-4a30-ae02-26d5af719688
ms.date: 12/05/2018
ms.keywords: ContextAdministratorForceMachine, ContextMachine, ContextUser, IX509EnrollmentPolicyServer interface [Security],Initialize method, IX509EnrollmentPolicyServer.Initialize, IX509EnrollmentPolicyServer::Initialize, Initialize, Initialize method [Security], Initialize method [Security],IX509EnrollmentPolicyServer interface, X509AuthAnonymous, X509AuthCertificate, X509AuthKerberos, X509AuthUsername, certenroll/IX509EnrollmentPolicyServer::Initialize, security.ix509enrollmentpolicyserver_initialize
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
 - IX509EnrollmentPolicyServer::Initialize
 - certenroll/IX509EnrollmentPolicyServer::Initialize
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
 - IX509EnrollmentPolicyServer.Initialize
---

# IX509EnrollmentPolicyServer::Initialize


## -description

The <b>Initialize</b> method initializes an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentpolicyserver">IX509EnrollmentPolicyServer</a> object.

## -parameters

### -param bstrPolicyServerUrl [in]

A <b>BSTR</b> variable that contains the URL for the certificate enrollment policy server.

### -param bstrPolicyServerId [in]

A <b>BSTR</b> variable that contains a unique ID for the certificate enrollment policy server. If this value is not <b>NULL</b>, it must match the ID string returned by the CEP response.

### -param authFlags [in]

An <a href="/windows/desktop/api/certcli/ne-certcli-x509enrollmentauthflags">X509EnrollmentAuthFlags</a> enumeration value that specifies the client authentication type. This can be one of the following values.

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

</td>
</tr>
<tr>
<td width="40%"><a id="X509AuthKerberos"></a><a id="x509authkerberos"></a><a id="X509AUTHKERBEROS"></a><dl>
<dt><b>X509AuthKerberos</b></dt>
</dl>
</td>
<td width="60%">
Kerberos authentication.

</td>
</tr>
<tr>
<td width="40%"><a id="X509AuthUsername"></a><a id="x509authusername"></a><a id="X509AUTHUSERNAME"></a><dl>
<dt><b>X509AuthUsername</b></dt>
</dl>
</td>
<td width="60%">
Clear text user name and password authentication.

<div class="alert"><b>Note</b>  The user name and password are encrypted before transmission and are stored securely in the credential vault on the CEP server.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="X509AuthCertificate"></a><a id="x509authcertificate"></a><a id="X509AUTHCERTIFICATE"></a><dl>
<dt><b>X509AuthCertificate</b></dt>
</dl>
</td>
<td width="60%">
Client authentication certificate installed on the local computer and used by the server to verify the identity of the client.

</td>
</tr>
</table>

### -param fIsUnTrusted [in]

A Boolean value that specifies whether to allow an untrusted certification authority certificates.

### -param context [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-x509certificateenrollmentcontext">X509CertificateEnrollmentContext</a> enumeration  value that specifies the nature of the end entity for which certificate enrollment is intended. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ContextUser"></a><a id="contextuser"></a><a id="CONTEXTUSER"></a><dl>
<dt><b>ContextUser</b></dt>
</dl>
</td>
<td width="60%">
The certificate is intended for an end user.

</td>
</tr>
<tr>
<td width="40%"><a id="ContextMachine"></a><a id="contextmachine"></a><a id="CONTEXTMACHINE"></a><dl>
<dt><b>ContextMachine</b></dt>
</dl>
</td>
<td width="60%">
The certificate is intended for a computer.

</td>
</tr>
<tr>
<td width="40%"><a id="ContextAdministratorForceMachine"></a><a id="contextadministratorforcemachine"></a><a id="CONTEXTADMINISTRATORFORCEMACHINE"></a><dl>
<dt><b>ContextAdministratorForceMachine</b></dt>
</dl>
</td>
<td width="60%">
The certificate is being requested by an administrator acting on the behalf of a computer.

</td>
</tr>
</table>

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
The <i>bstrPolicyServerUrl</i> parameter cannot be an empty string and must represent an HTTPS URL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not sufficient memory available for the strings specified in the <i>bstrPolicyServerUrl</i> or <i>bstrPolicyServerId</i> parameters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentpolicyserver">IX509EnrollmentPolicyServer</a> object has already been initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_DATA)</b></dt>
</dl>
</td>
<td width="60%">
The value specified in the <i>bstrPolicyServerId</i> parameter is not <b>NULL</b> and does not equal the existing CEP ID value on the CEP server.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentpolicyserver">IX509EnrollmentPolicyServer</a>