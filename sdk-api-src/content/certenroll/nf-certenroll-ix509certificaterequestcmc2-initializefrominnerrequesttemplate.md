---
UID: NF:certenroll.IX509CertificateRequestCmc2.InitializeFromInnerRequestTemplate
title: IX509CertificateRequestCmc2::InitializeFromInnerRequestTemplate (certenroll.h)
description: Initializes the certificate request from an inner request object and a template.
helpviewer_keywords: ["IX509CertificateRequestCmc2 interface [Security]","InitializeFromInnerRequestTemplate method","IX509CertificateRequestCmc2.InitializeFromInnerRequestTemplate","IX509CertificateRequestCmc2::InitializeFromInnerRequestTemplate","InitializeFromInnerRequestTemplate","InitializeFromInnerRequestTemplate method [Security]","InitializeFromInnerRequestTemplate method [Security]","IX509CertificateRequestCmc2 interface","certenroll/IX509CertificateRequestCmc2::InitializeFromInnerRequestTemplate","security.ix509certificaterequestcmc2_initializefrominnerrequesttemplate"]
old-location: security\ix509certificaterequestcmc2_initializefrominnerrequesttemplate.htm
tech.root: security
ms.assetid: 12490859-bb4a-49ff-9d92-24bf04ab3999
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestCmc2 interface [Security],InitializeFromInnerRequestTemplate method, IX509CertificateRequestCmc2.InitializeFromInnerRequestTemplate, IX509CertificateRequestCmc2::InitializeFromInnerRequestTemplate, InitializeFromInnerRequestTemplate, InitializeFromInnerRequestTemplate method [Security], InitializeFromInnerRequestTemplate method [Security],IX509CertificateRequestCmc2 interface, certenroll/IX509CertificateRequestCmc2::InitializeFromInnerRequestTemplate, security.ix509certificaterequestcmc2_initializefrominnerrequesttemplate
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
 - IX509CertificateRequestCmc2::InitializeFromInnerRequestTemplate
 - certenroll/IX509CertificateRequestCmc2::InitializeFromInnerRequestTemplate
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
 - IX509CertificateRequestCmc2.InitializeFromInnerRequestTemplate
---

# IX509CertificateRequestCmc2::InitializeFromInnerRequestTemplate


## -description

The <b>InitializeFromInnerRequestTemplate</b> method initializes the certificate request from an inner request  object and a template.

## -parameters

### -param pInnerRequest [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a> interface that represents the inner request object. This can be a PKCS #10 or  a CMC request.

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
<dt><b>CRYPT_E_INVALID_MSG_TYPE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The request object passed to the <i>pInnerRequest</i> parameter must be a PKCS #10 or a CMC request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pInnerRequest</i>, <i>pPolicyServer</i>, and <i>pTemplate</i> parameters cannot be <b>NULL</b>.

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
The request object has already been initialized.

</td>
</tr>
</table>

## -remarks

By specifying a template, you can add information to the outer request object that may not be contained in the inner request. For example, if the inner request does not contain the necessary extensions, you can supply a template that does.

The <b>InitializeFromInnerRequestTemplate</b> method:<ul>
<li>Creates an empty <a href="/windows/desktop/api/certenroll/nn-certenroll-icryptattributes">ICryptAttributes</a> collection.</li>
<li>Creates an empty <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509namevaluepairs">IX509NameValuePairs</a> collection.</li>
<li>Creates an empty <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection.</li>
<li>Creates an <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectids">IObjectIds</a> collection for  critical extensions and adds the XCN_OID_KEY_USAGE and XCN_OID_BASIC_CONSTRAINTS2 object identifiers (OIDs).</li>
<li>Creates an empty <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectids">IObjectIds</a> collection of OIDs to be suppressed from the request object.</li>
<li>Creates an empty <a href="/windows/desktop/api/certenroll/nn-certenroll-isignercertificates">ISignerCertificates</a> collection.</li>
<li>Retrieves private key flags from the template.</li>
<li>Sets the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey">ArchivePrivateKey</a> property if required by the template flags or settings.</li>
<li>Retrieves the encryption algorithm from the template if one is specified and sets the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-get_encryptionalgorithm">EncryptionAlgorithm</a> property.</li>
<li>Sets the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-get_encryptionstrength">EncryptionStrength</a> property if possible.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc2">IX509CertificateRequestCmc2</a>