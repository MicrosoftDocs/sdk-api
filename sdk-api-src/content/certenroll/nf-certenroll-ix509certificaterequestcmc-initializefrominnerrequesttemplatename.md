---
UID: NF:certenroll.IX509CertificateRequestCmc.InitializeFromInnerRequestTemplateName
title: IX509CertificateRequestCmc::InitializeFromInnerRequestTemplateName (certenroll.h)
description: The InitializeFromInnerRequestTemplateName method initializes the certificate request from an inner request object and a template.
helpviewer_keywords: ["IX509CertificateRequestCmc interface [Security]","InitializeFromInnerRequestTemplateName method","IX509CertificateRequestCmc.InitializeFromInnerRequestTemplateName","IX509CertificateRequestCmc::InitializeFromInnerRequestTemplateName","InitializeFromInnerRequestTemplateName","InitializeFromInnerRequestTemplateName method [Security]","InitializeFromInnerRequestTemplateName method [Security]","IX509CertificateRequestCmc interface","certenroll/IX509CertificateRequestCmc::InitializeFromInnerRequestTemplateName","security.ix509certificaterequestcmc_initializefrominnerrequesttemplatename"]
old-location: security\ix509certificaterequestcmc_initializefrominnerrequesttemplatename.htm
tech.root: security
ms.assetid: abf7617e-1194-4303-a214-23fbaf20eccf
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],InitializeFromInnerRequestTemplateName method, IX509CertificateRequestCmc.InitializeFromInnerRequestTemplateName, IX509CertificateRequestCmc::InitializeFromInnerRequestTemplateName, InitializeFromInnerRequestTemplateName, InitializeFromInnerRequestTemplateName method [Security], InitializeFromInnerRequestTemplateName method [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::InitializeFromInnerRequestTemplateName, security.ix509certificaterequestcmc_initializefrominnerrequesttemplatename
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
 - IX509CertificateRequestCmc::InitializeFromInnerRequestTemplateName
 - certenroll/IX509CertificateRequestCmc::InitializeFromInnerRequestTemplateName
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
 - IX509CertificateRequestCmc.InitializeFromInnerRequestTemplateName
---

# IX509CertificateRequestCmc::InitializeFromInnerRequestTemplateName


## -description

The <b>InitializeFromInnerRequestTemplateName</b> method initializes the certificate request from an inner request  object and a template.

## -parameters

### -param pInnerRequest [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a> interface that represents the inner request object. This can be a PKCS #10 or  a CMC request.

### -param strTemplateName [in]

A <b>BSTR</b> variable that contains the Common Name (CN) of the template as it appears in Active Directory or the dotted decimal <a href="/windows/desktop/SecGloss/o-gly">object identifier</a>.

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

The <b>InitializeFromInnerRequestTemplateName</b> method:<ul>
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

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>