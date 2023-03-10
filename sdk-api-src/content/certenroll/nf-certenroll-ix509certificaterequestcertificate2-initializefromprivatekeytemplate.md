---
UID: NF:certenroll.IX509CertificateRequestCertificate2.InitializeFromPrivateKeyTemplate
title: IX509CertificateRequestCertificate2::InitializeFromPrivateKeyTemplate (certenroll.h)
description: Initializes the certificate request by using an IX509PrivateKey object and a certificate template. (IX509CertificateRequestCertificate2.InitializeFromPrivateKeyTemplate)
helpviewer_keywords: ["ContextAdministratorForceMachine","ContextMachine","ContextUser","IX509CertificateRequestCertificate2 interface [Security]","InitializeFromPrivateKeyTemplate method","IX509CertificateRequestCertificate2.InitializeFromPrivateKeyTemplate","IX509CertificateRequestCertificate2::InitializeFromPrivateKeyTemplate","InitializeFromPrivateKeyTemplate","InitializeFromPrivateKeyTemplate method [Security]","InitializeFromPrivateKeyTemplate method [Security]","IX509CertificateRequestCertificate2 interface","certenroll/IX509CertificateRequestCertificate2::InitializeFromPrivateKeyTemplate","security.ix509certificaterequestcertificate2_initializefromprivatekeytemplate"]
old-location: security\ix509certificaterequestcertificate2_initializefromprivatekeytemplate.htm
tech.root: security
ms.assetid: 334cc5f7-e74e-4f0b-b54b-6f1b121418da
ms.date: 12/05/2018
ms.keywords: ContextAdministratorForceMachine, ContextMachine, ContextUser, IX509CertificateRequestCertificate2 interface [Security],InitializeFromPrivateKeyTemplate method, IX509CertificateRequestCertificate2.InitializeFromPrivateKeyTemplate, IX509CertificateRequestCertificate2::InitializeFromPrivateKeyTemplate, InitializeFromPrivateKeyTemplate, InitializeFromPrivateKeyTemplate method [Security], InitializeFromPrivateKeyTemplate method [Security],IX509CertificateRequestCertificate2 interface, certenroll/IX509CertificateRequestCertificate2::InitializeFromPrivateKeyTemplate, security.ix509certificaterequestcertificate2_initializefromprivatekeytemplate
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
 - IX509CertificateRequestCertificate2::InitializeFromPrivateKeyTemplate
 - certenroll/IX509CertificateRequestCertificate2::InitializeFromPrivateKeyTemplate
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
 - IX509CertificateRequestCertificate2.InitializeFromPrivateKeyTemplate
---

# IX509CertificateRequestCertificate2::InitializeFromPrivateKeyTemplate


## -description

The <b>InitializeFromPrivateKeyTemplate</b> method initializes the certificate request by using an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> object and a certificate template.

## -parameters

### -param Context [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-x509certificateenrollmentcontext">X509CertificateEnrollmentContext</a> enumeration value that specifies whether the requested certificate is intended for an end user, a computer, or an administrator acting on behalf of the computer. This can be one of the following values. However, if the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_machinecontext">MachineContext</a> property of the <a href="/windows/desktop/SecGloss/p-gly">private key</a> is set, you must specify the <b>ContextMachine</b> enumeration value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ContextUser"></a><a id="contextuser"></a><a id="CONTEXTUSER"></a><dl>
<dt><b>ContextUser</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The certificate is being requested for an end user.

</td>
</tr>
<tr>
<td width="40%"><a id="ContextMachine"></a><a id="contextmachine"></a><a id="CONTEXTMACHINE"></a><dl>
<dt><b>ContextMachine</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The certificate is being requested for a computer.

</td>
</tr>
<tr>
<td width="40%"><a id="ContextAdministratorForceMachine"></a><a id="contextadministratorforcemachine"></a><a id="CONTEXTADMINISTRATORFORCEMACHINE"></a><dl>
<dt><b>ContextAdministratorForceMachine</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The certificate is being requested by an administrator acting on the behalf of a computer.

</td>
</tr>
</table>

### -param pPrivateKey [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> interface that represents the private key.

### -param pPolicyServer [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentpolicyserver">IX509EnrollmentPolicyServer</a> object that represents the certificate enrollment policy (CEP) server that contains the template specified by the <i>pTemplate</i> parameter.

### -param pTemplate [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificatetemplate">IX509CertificateTemplate</a> object that represents the template to use during initialization.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pPrivateKey</i>, <i>pPolicyServer</i>, or <i>pTemplate</i> parameters are <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></dt>
</dl>
</td>
<td width="60%">
The certificate request object has already been initialized.

</td>
</tr>
</table>

## -remarks

The <b>InitializeFromPrivateKeyTemplate</b> method performs the following actions:<ul>
<li>Adds the extensions specified by the template to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection.</li>
<li>Creates an <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectids">IObjectIds</a> collection and populates it with the default XCN_OID_KEY_USAGE and XCN_OID_BASIC_CONSTRAINTS2 object identifiers. If the template indicates that these OIDs are not critical, they are removed from the collection. The OIDs marked critical by the template are added.</li>
<li>Sets the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_smimecapabilities">SmimeCapabilities</a> property if the template supports symmetric algorithms.</li>
<li>Sets the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm">AlternateSignatureAlgorithm</a> property if the template requires a discrete signature algorithm OID.</li>
<li>Creates an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a> object.</li>
<li>Creates a hash algorithm OID if the algorithm is specified in the template and sets it on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a> object.</li>
<li>Retrieves an asymmetric encryption algorithm OID, if it exists, from the template and sets it on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a> object.</li>
<li>Populates many of the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> properties from the template settings.</li>
</ul>


If the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_cspinformations">CSPInformations</a> property is not specified, the method creates an <a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformations">ICspInformations</a> collection from the providers installed on the computer.

No private key is created at this point. If the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> object passed to the method does not represent an existing key, a key is created when the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method is called. The key will be created by using the default provider if no template was specified and the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_providername">ProviderName</a> property on the <b>IX509PrivateKey</b> is not set. When a private key exists, it is set on the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_privatekey">PrivateKey</a> property.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcertificate2">IX509CertificateRequestCertificate2</a>
