---
UID: NF:certenroll.IX509Enrollment2.InstallResponse2
title: IX509Enrollment2::InstallResponse2 (certenroll.h)
description: Installs a certificate chain on the end-entity computer. (IX509Enrollment2.InstallResponse2)
helpviewer_keywords: ["AllowNoOutstandingRequest","AllowNone","AllowUntrustedCertificate","AllowUntrustedRoot","IX509Enrollment2 interface [Security]","InstallResponse2 method","IX509Enrollment2.InstallResponse2","IX509Enrollment2::InstallResponse2","InstallResponse2","InstallResponse2 method [Security]","InstallResponse2 method [Security]","IX509Enrollment2 interface","PsfAllowUnTrustedCA","PsfAutoEnrollmentEnabled","PsfLocationGroupPolicy","PsfLocationRegistry","PsfUseClientId","X509AuthAnonymous","X509AuthCertificate","X509AuthKerberos","X509AuthUsername","certenroll/IX509Enrollment2::InstallResponse2","security.ix509enrollment2_installresponse2"]
old-location: security\ix509enrollment2_installresponse2.htm
tech.root: security
ms.assetid: 1a5dce88-afc5-4d47-85e8-980192a662d8
ms.date: 12/05/2018
ms.keywords: AllowNoOutstandingRequest, AllowNone, AllowUntrustedCertificate, AllowUntrustedRoot, IX509Enrollment2 interface [Security],InstallResponse2 method, IX509Enrollment2.InstallResponse2, IX509Enrollment2::InstallResponse2, InstallResponse2, InstallResponse2 method [Security], InstallResponse2 method [Security],IX509Enrollment2 interface, PsfAllowUnTrustedCA, PsfAutoEnrollmentEnabled, PsfLocationGroupPolicy, PsfLocationRegistry, PsfUseClientId, X509AuthAnonymous, X509AuthCertificate, X509AuthKerberos, X509AuthUsername, certenroll/IX509Enrollment2::InstallResponse2, security.ix509enrollment2_installresponse2
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
 - IX509Enrollment2::InstallResponse2
 - certenroll/IX509Enrollment2::InstallResponse2
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
 - IX509Enrollment2.InstallResponse2
---

# IX509Enrollment2::InstallResponse2


## -description

The <b>InstallResponse2</b> method installs a certificate chain on the end-entity computer. The byte array that contains the response is encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) as defined by the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) standard.  You must specify  the DER-encoded byte array in a string that is either a pure binary sequence or is Unicode encoded. This method is web enabled.

## -parameters

### -param Restrictions [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-installresponserestrictionflags">InstallResponseRestrictionFlags</a> enumeration value that specifies the type of certificates that can be installed. This can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AllowNone"></a><a id="allownone"></a><a id="ALLOWNONE"></a><dl>
<dt><b>AllowNone</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Do not install untrusted certificates or certificates for which there is no corresponding request.

</td>
</tr>
<tr>
<td width="40%"><a id="AllowNoOutstandingRequest"></a><a id="allownooutstandingrequest"></a><a id="ALLOWNOOUTSTANDINGREQUEST"></a><dl>
<dt><b>AllowNoOutstandingRequest</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Create the <a href="/windows/desktop/SecGloss/p-gly">private key</a> from the certificate response rather than from the dummy certificate. This makes the dummy certificate optional. If this value is not set, the dummy certificate must exist, and the private key is extracted from it.

</td>
</tr>
<tr>
<td width="40%"><a id="AllowUntrustedCertificate"></a><a id="allowuntrustedcertificate"></a><a id="ALLOWUNTRUSTEDCERTIFICATE"></a><dl>
<dt><b>AllowUntrustedCertificate</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Install untrusted end entity and <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> certificates. Certification authority certificates include root and subordinate CA certificates. End entity certificates are installed to the personal store, and CA certificates are installed to the certification authority store.

</td>
</tr>
<tr>
<td width="40%"><a id="AllowUntrustedRoot"></a><a id="allowuntrustedroot"></a><a id="ALLOWUNTRUSTEDROOT"></a><dl>
<dt><b>AllowUntrustedRoot</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Perform the same action as the <b>AllowUntrustedCertificate</b> flag but also installs the certificate even if the certificate chain cannot be built because the root is not trusted. <div class="alert"><b>Note</b>  On Windows Vista, the behavior of this flag is the same as that defined for the <b>AllowUntrustedCertificate</b> flag. You can install an untrusted root beginning with Windows Vista with SP1.</div>
<div> </div>


</td>
</tr>
</table>

### -param strResponse [in]

A <b>BSTR</b> variable that contains the DER-encoded response.

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of encoding applied to  the string that contains the DER-encoded response.

### -param strPassword [in, optional]

An optional password for the certificate installation. This can be  <b>NULL</b> to indicate that  no password is used.  When you have finished using the password, clear it from memory by calling the <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function. For more information about protecting the password, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.

### -param strEnrollmentPolicyServerUrl [in]

A <b>BSTR</b> that contains the URL of the certificate enrollment policy (CEP) server.

### -param strEnrollmentPolicyServerID [in]

A <b>BSTR</b> that contains an identifier for the CEP server.

### -param EnrollmentPolicyServerFlags [in]

A <a href="/windows/desktop/api/certenroll/ne-certenroll-policyserverurlflags">PolicyServerUrlFlags</a> enumeration value. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PsfLocationGroupPolicy"></a><a id="psflocationgrouppolicy"></a><a id="PSFLOCATIONGROUPPOLICY"></a><dl>
<dt><b>PsfLocationGroupPolicy</b></dt>
</dl>
</td>
<td width="60%">
The CEP server URL is specified in group policy by an administrator.

</td>
</tr>
<tr>
<td width="40%"><a id="PsfLocationRegistry"></a><a id="psflocationregistry"></a><a id="PSFLOCATIONREGISTRY"></a><dl>
<dt><b>PsfLocationRegistry</b></dt>
</dl>
</td>
<td width="60%">
The CEP server URL is specified in the registry.

</td>
</tr>
<tr>
<td width="40%"><a id="PsfUseClientId"></a><a id="psfuseclientid"></a><a id="PSFUSECLIENTID"></a><dl>
<dt><b>PsfUseClientId</b></dt>
</dl>
</td>
<td width="60%">
Specifies that certificate enrollments and renewals include client specific data in a <b>ClientId</b> attribute. Examples include the name of the cryptographic service provider, the Windows version number, the user name, the computer DNS name, and the domain controller DNS name. This flag can be set by group policy.

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

### -param authFlags [in]

An <a href="/windows/desktop/api/certcli/ne-certcli-x509enrollmentauthflags">X509EnrollmentAuthFlags</a> enumeration value that specifies the client authentication type. For Windows 7, only <b>X509AuthCertificate</b> can be chosen from the following values.

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

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This method was called from the web and either <b>AllowNoOutstandingRequest</b> or <b>AllowUntrustedCertificate</b> was specified in the <i>Restrictions</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ARITHMETIC_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The length of the string that contains the password exceeds 64 kilobytes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_BLANK</b></dt>
</dl>
</td>
<td width="60%">
The enrollment object has not been initialized.

</td>
</tr>
</table>

## -remarks

The <b>InstallResponse2</b> method:

<ol>
<li>Retrieves the dummy certificate from the external store.</li>
<li>Retrieves the certificate contained in the response and installs it on the computer.</li>
<li>Copies properties from the dummy certificate in the external store onto the newly installed certificate in the personal store.</li>
</ol>


Before calling the <b>InstallResponse2</b> method, you must initialize the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a> object by calling one of the following methods.<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-initialize">Initialize</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-initializefromrequest">InitializeFromRequest</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment2-initializefromtemplate">InitializeFromTemplate</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-initializefromtemplatename">InitializeFromTemplateName</a>
</li>
</ul>


If you call this method from the web, you can specify only <b>AllowNone</b> or <b>AllowUntrustedRoot</b> in the <i>Restrictions</i> parameter. If you specify <b>AllowNoOutstandingRequest</b> or <b>AllowUntrustedCertificate</b>, the method returns an <b>E_ACCESSDENIED</b> error.

The last four parameters (<i>strEnrollmentPolicyServerUrl</i>, <i>strEnrollmentPolicyServerID</i>, <i>EnrollmentPolicyServerFlags</i>, and <i>authFlags</i>) are not included in the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-installresponse">InstallResponse</a> method. They enable you to add a property value to the installed certificate in much the same way as the <a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyenrollmentpolicyserver">ICertPropertyEnrollmentPolicyServer</a> interface does.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment2">IX509Enrollment2</a>
