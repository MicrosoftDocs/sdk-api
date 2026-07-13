---
UID: NF:certenroll.IX509Enrollment.InstallResponse
title: IX509Enrollment::InstallResponse (certenroll.h)
description: Installs a certificate chain on the end-entity computer. (IX509Enrollment.InstallResponse)
helpviewer_keywords: ["AllowNoOutstandingRequest","AllowNone","AllowUntrustedCertificate","AllowUntrustedRoot","IX509Enrollment interface [Security]","InstallResponse method","IX509Enrollment.InstallResponse","IX509Enrollment::InstallResponse","InstallResponse","InstallResponse method [Security]","InstallResponse method [Security]","IX509Enrollment interface","certenroll/IX509Enrollment::InstallResponse","security.ix509enrollment_installresponse_method"]
old-location: security\ix509enrollment_installresponse_method.htm
tech.root: security
ms.assetid: 4ad33092-71c4-4ae1-a3a6-cef376d04c2d
ms.date: 12/05/2018
ms.keywords: AllowNoOutstandingRequest, AllowNone, AllowUntrustedCertificate, AllowUntrustedRoot, IX509Enrollment interface [Security],InstallResponse method, IX509Enrollment.InstallResponse, IX509Enrollment::InstallResponse, InstallResponse, InstallResponse method [Security], InstallResponse method [Security],IX509Enrollment interface, certenroll/IX509Enrollment::InstallResponse, security.ix509enrollment_installresponse_method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509Enrollment::InstallResponse
 - certenroll/IX509Enrollment::InstallResponse
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509Enrollment.InstallResponse
---

# IX509Enrollment::InstallResponse


## -description

The <b>InstallResponse</b> method installs a certificate chain on the end-entity computer. The byte array that contains the response is encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) as defined by the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) standard.  You must specify  the DER-encoded byte array in a string that is either a pure binary sequence or is Unicode encoded. This method is web enabled.

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
Perform the same action as the <b>AllowUntrustedCertificate</b> flag but also installs the certificate even if the certificate chain cannot be built because the root is not trusted. <div class="alert"><b>Note</b>  On Windows Vista, the behavior of this flag is the same as that defined for the <b>AllowUntrustedCertificate</b> flag. Beginning with Windows Vista with SP1, you can install a certificate that chains up to an untrusted root.</div>
<div> </div>


</td>
</tr>
</table>

### -param strResponse [in]

A <b>BSTR</b> variable that contains the DER-encoded response.

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of encoding applied to  the string that contains the DER-encoded response.

### -param strPassword [in, optional]

An optional password for the certificate installation. This can be  <b>NULL</b> or an empty string to indicate that  no password is used.  If there is a password, clear it from memory when you have finished using it by calling the <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function. For more information about protecting the password, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.

Beginning with Windows 8 and Windows Server 2012, a <b>NULL</b> or empty password may mean that the PFX packet was created in the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-pfxexportcertstoreex">PFXExportCertStoreEx</a> function by using the <b>PKCS12_PROTECT_TO_DOMAIN_SIDS</b> flag. If so, the PFX was encrypted to an Active Directory group. For more information, see  <b>PFXExportCertStoreEx</b> and <a href="/windows/desktop/api/wincrypt/nf-wincrypt-pfximportcertstore">PFXImportCertStore</a>.

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

The <b>InstallResponse</b> method:

<ol>
<li>Retrieves the dummy certificate from the external store.</li>
<li>Retrieves the certificate contained in the response and installs it on the computer.</li>
<li>Copies properties from the dummy certificate in the external store onto the newly installed certificate in the personal store.</li>
</ol>


Before calling the <b>InstallResponse</b> method, you must initialize the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a> object by calling one of the following methods.<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-initialize">Initialize</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-initializefromrequest">InitializeFromRequest</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-initializefromtemplatename">InitializeFromTemplateName</a>
</li>
</ul>


If you call this method from the web, you can specify only <b>AllowNone</b> or <b>AllowUntrustedRoot</b> in the <i>Restrictions</i> parameter. If you specify <b>AllowNoOutstandingRequest</b> or <b>AllowUntrustedCertificate</b>, the method returns an <b>E_ACCESSDENIED</b> error.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a>
