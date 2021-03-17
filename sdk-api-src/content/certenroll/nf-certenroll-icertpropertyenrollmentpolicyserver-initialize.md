---
UID: NF:certenroll.ICertPropertyEnrollmentPolicyServer.Initialize
title: ICertPropertyEnrollmentPolicyServer::Initialize (certenroll.h)
description: Initializes an ICertPropertyEnrollmentPolicyServer object.
helpviewer_keywords: ["DefaultNone","DefaultPolicyServer","ICertPropertyEnrollmentPolicyServer interface [Security]","Initialize method","ICertPropertyEnrollmentPolicyServer.Initialize","ICertPropertyEnrollmentPolicyServer::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","ICertPropertyEnrollmentPolicyServer interface","PsfAllowUnTrustedCA","PsfAutoEnrollmentEnabled","PsfLocationGroupPolicy","PsfLocationRegistry","PsfNone","PsfUseClientId","X509AuthAnonymous","X509AuthCertificate","X509AuthKerberos","X509AuthUsername","certenroll/ICertPropertyEnrollmentPolicyServer::Initialize","security.icertpropertyenrollmentpolicyserver_initialize"]
old-location: security\icertpropertyenrollmentpolicyserver_initialize.htm
tech.root: security
ms.assetid: 5d54ffb2-4a81-4d52-80db-b8526a52bb53
ms.date: 12/05/2018
ms.keywords: DefaultNone, DefaultPolicyServer, ICertPropertyEnrollmentPolicyServer interface [Security],Initialize method, ICertPropertyEnrollmentPolicyServer.Initialize, ICertPropertyEnrollmentPolicyServer::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertPropertyEnrollmentPolicyServer interface, PsfAllowUnTrustedCA, PsfAutoEnrollmentEnabled, PsfLocationGroupPolicy, PsfLocationRegistry, PsfNone, PsfUseClientId, X509AuthAnonymous, X509AuthCertificate, X509AuthKerberos, X509AuthUsername, certenroll/ICertPropertyEnrollmentPolicyServer::Initialize, security.icertpropertyenrollmentpolicyserver_initialize
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
 - ICertPropertyEnrollmentPolicyServer::Initialize
 - certenroll/ICertPropertyEnrollmentPolicyServer::Initialize
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
 - ICertPropertyEnrollmentPolicyServer.Initialize
---

# ICertPropertyEnrollmentPolicyServer::Initialize


## -description

The <b>Initialize</b> method initializes an <a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyenrollmentpolicyserver">ICertPropertyEnrollmentPolicyServer</a> object.

## -parameters

### -param PropertyFlags [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-enrollmentpolicyserverpropertyflags">EnrollmentPolicyServerPropertyFlags</a> enumeration value that specifies the default certificate enrollment policy (CEP) server. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DefaultNone"></a><a id="defaultnone"></a><a id="DEFAULTNONE"></a><dl>
<dt><b>DefaultNone</b></dt>
</dl>
</td>
<td width="60%">
No default policy server URL has been specified.

</td>
</tr>
<tr>
<td width="40%"><a id="DefaultPolicyServer"></a><a id="defaultpolicyserver"></a><a id="DEFAULTPOLICYSERVER"></a><dl>
<dt><b>DefaultPolicyServer</b></dt>
</dl>
</td>
<td width="60%">
The policy server URL returned by <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollmentpolicyserver-getpolicyserverurl">GetPolicyServerUrl</a> is the default value when an URL has not been specified.

</td>
</tr>
</table>

### -param AuthFlags [in]

An <a href="/windows/desktop/api/certcli/ne-certcli-x509enrollmentauthflags">X509EnrollmentAuthFlags</a> enumeration value that specifies the authentication type used by the client to authenticate itself to the CEP server. This can be one of the following values.

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

<div class="alert"><b>Note</b>  The user name and password are encrypted before transmission and are stored securely in the credential vault on the server.</div>
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

### -param EnrollmentServerAuthFlags [in]

An <a href="/windows/desktop/api/certcli/ne-certcli-x509enrollmentauthflags">X509EnrollmentAuthFlags</a> enumeration value that specifies the authentication type used by the client to authenticate itself to the CES. See the <i>AuthFlags</i> parameter for the possible values of the enumeration type. For Windows 7, only <b>X509AuthCertificate</b> can be specified.

### -param UrlFlags [in]

A <a href="/windows/desktop/api/certenroll/ne-certenroll-policyserverurlflags">PolicyServerUrlFlags</a> enumeration value that specifies policy server flags. This can be a bitwise <b>OR</b> of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PsfNone"></a><a id="psfnone"></a><a id="PSFNONE"></a><dl>
<dt><b>PsfNone</b></dt>
</dl>
</td>
<td width="60%">
No flags are specified.

</td>
</tr>
<tr>
<td width="40%"><a id="PsfLocationGroupPolicy"></a><a id="psflocationgrouppolicy"></a><a id="PSFLOCATIONGROUPPOLICY"></a><dl>
<dt><b>PsfLocationGroupPolicy</b></dt>
</dl>
</td>
<td width="60%">
The policy server URL is specified in group policy by an administrator.

</td>
</tr>
<tr>
<td width="40%"><a id="PsfLocationRegistry"></a><a id="psflocationregistry"></a><a id="PSFLOCATIONREGISTRY"></a><dl>
<dt><b>PsfLocationRegistry</b></dt>
</dl>
</td>
<td width="60%">
The policy server URL is specified in the registry.

</td>
</tr>
<tr>
<td width="40%"><a id="PsfUseClientId"></a><a id="psfuseclientid"></a><a id="PSFUSECLIENTID"></a><dl>
<dt><b>PsfUseClientId</b></dt>
</dl>
</td>
<td width="60%">
Specifies that certificate enrollments and renewals include client specific data in a <b>ClientId</b> attribute. Examples include the name of the cryptographic service provider, the Windows version number, the user name, the computer DNS name, and the domain controller DNS name.

This flag has been included to address privacy concerns that can arise during enrollment to servers that are managed by administrators other than those who manage the forest in which the user resides. By not setting this flag, you can prevent sending personal information to non-local administrators.

</td>
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

### -param strRequestId [in]

 A <b>BSTR</b> variable that contains a unique string identifier for the certificate request to be sent to the certification authority during enrollment. The string can contain any information that uniquely identifies the request.

### -param strUrl [in]

 A <b>BSTR</b> variable that contains the URL for the certificate enrollment policy (CEP) server.

### -param strId [in]

A <b>BSTR</b> variable that contains the ID of the CEP server.

### -param strEnrollmentServerUrl [in]

A <b>BSTR</b> variable that contains the URL for the certificate enrollment server.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory available to a string value.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyenrollmentpolicyserver">ICertPropertyEnrollmentPolicyServer</a>