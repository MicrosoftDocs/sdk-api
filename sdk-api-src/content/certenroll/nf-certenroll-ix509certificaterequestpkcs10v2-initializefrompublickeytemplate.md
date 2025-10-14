---
UID: NF:certenroll.IX509CertificateRequestPkcs10V2.InitializeFromPublicKeyTemplate
title: IX509CertificateRequestPkcs10V2::InitializeFromPublicKeyTemplate (certenroll.h)
description: Initializes a null-signed certificate request by using an IX509PublicKey object and a template.
helpviewer_keywords: ["ContextAdministratorForceMachine","ContextMachine","ContextUser","IX509CertificateRequestPkcs10V2 interface [Security]","InitializeFromPublicKeyTemplate method","IX509CertificateRequestPkcs10V2.InitializeFromPublicKeyTemplate","IX509CertificateRequestPkcs10V2::InitializeFromPublicKeyTemplate","InitializeFromPublicKeyTemplate","InitializeFromPublicKeyTemplate method [Security]","InitializeFromPublicKeyTemplate method [Security]","IX509CertificateRequestPkcs10V2 interface","certenroll/IX509CertificateRequestPkcs10V2::InitializeFromPublicKeyTemplate","security.ix509certificaterequestpkcs10v2_initializefrompublickeytemplate"]
old-location: security\ix509certificaterequestpkcs10v2_initializefrompublickeytemplate.htm
tech.root: security
ms.assetid: 20e94948-1455-46c4-bc8c-55dfde45818c
ms.date: 12/05/2018
ms.keywords: ContextAdministratorForceMachine, ContextMachine, ContextUser, IX509CertificateRequestPkcs10V2 interface [Security],InitializeFromPublicKeyTemplate method, IX509CertificateRequestPkcs10V2.InitializeFromPublicKeyTemplate, IX509CertificateRequestPkcs10V2::InitializeFromPublicKeyTemplate, InitializeFromPublicKeyTemplate, InitializeFromPublicKeyTemplate method [Security], InitializeFromPublicKeyTemplate method [Security],IX509CertificateRequestPkcs10V2 interface, certenroll/IX509CertificateRequestPkcs10V2::InitializeFromPublicKeyTemplate, security.ix509certificaterequestpkcs10v2_initializefrompublickeytemplate
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
 - IX509CertificateRequestPkcs10V2::InitializeFromPublicKeyTemplate
 - certenroll/IX509CertificateRequestPkcs10V2::InitializeFromPublicKeyTemplate
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
 - IX509CertificateRequestPkcs10V2.InitializeFromPublicKeyTemplate
---

# IX509CertificateRequestPkcs10V2::InitializeFromPublicKeyTemplate


## -description

The <b>InitializeFromPublicKeyTemplate</b> method initializes a null-signed certificate request by using an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509publickey">IX509PublicKey</a> object and a template.

## -parameters

### -param Context [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-x509certificateenrollmentcontext">X509CertificateEnrollmentContext</a> enumeration value that specifies whether the requested certificate is intended for an end user, a computer, or an administrator acting on behalf of the computer. This can be one of the following values.

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

### -param pPublicKey [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509publickey">IX509PublicKey</a> interface that represents the public key.

### -param pPolicyServer [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentpolicyserver">IX509EnrollmentPolicyServer</a> object that represents the certificate enrollment policy (CEP) server that contains the template specified by the <i>pTemplate</i> parameter.

### -param pTemplate [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificatetemplate">IX509CertificateTemplate</a> object that represents the template to use during initialization.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pPublicKey</i>, <i>pPolicyServer</i>, or <i>pTemplate</i> parameters are <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The certificate request object has already been initialized.

</td>
</tr>
</table>

## -remarks

The <b>InitializeFromPublicKeyTemplate</b> method performs the following actions:<ul>
<li>Adds the extensions specified in the template, if any, to the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection.</li>
<li>Creates a <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_criticalextensions">CriticalExtensions</a> collection and populates it with the default XCN_OID_KEY_USAGE and XCN_OID_BASIC_CONSTRAINTS2 object identifiers. If the template indicates that these OIDs are not critical, they are removed from the collection. The OIDs marked critical by the template, if any,  are added.</li>
<li>Sets the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_smimecapabilities">SmimeCapabilities</a> property if the template supports symmetric algorithms.</li>
<li>Sets the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm">AlternateSignatureAlgorithm</a> property if the template requires a discrete signature algorithm OID.</li>
<li>Creates an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a> object.</li>
<li>Creates a hash algorithm OID if the algorithm is specified in the template and sets it on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a> object.</li>
<li>Creates an asymmetric encryption algorithm OID if the algorithm is specified in the template and sets it on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a> object.</li>
</ul>


If the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_cspinformations">CSPInformations</a> property is not specified, the method creates an <a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformations">ICspInformations</a> collection from the providers installed on the computer.

The method does not create a private key. The use of this method implies that the request is null-signed. Therefore, the method sets the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_nullsigned">NullSigned</a> property on the  <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a> object.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10v2">IX509CertificateRequestPkcs10V2</a>