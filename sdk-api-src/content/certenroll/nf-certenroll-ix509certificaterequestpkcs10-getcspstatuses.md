---
UID: NF:certenroll.IX509CertificateRequestPkcs10.GetCspStatuses
title: IX509CertificateRequestPkcs10::GetCspStatuses (certenroll.h)
description: Retrieves an ICspStatuses collection that contains all provider/algorithm pairs consistent with the intended use of the private key as specified by the caller.
helpviewer_keywords: ["GetCspStatuses","GetCspStatuses method [Security]","GetCspStatuses method [Security]","IX509CertificateRequestPkcs10 interface","IX509CertificateRequestPkcs10 interface [Security]","GetCspStatuses method","IX509CertificateRequestPkcs10.GetCspStatuses","IX509CertificateRequestPkcs10::GetCspStatuses","XCN_AT_KEYEXCHANGE","XCN_AT_NONE","XCN_AT_SIGNATURE","certenroll/IX509CertificateRequestPkcs10::GetCspStatuses","security.ix509certificaterequestpkcs10_getcspstatuses_method"]
old-location: security\ix509certificaterequestpkcs10_getcspstatuses_method.htm
tech.root: security
ms.assetid: 50dc8cc5-21ee-4347-a12a-0d6e62901fbb
ms.date: 12/05/2018
ms.keywords: GetCspStatuses, GetCspStatuses method [Security], GetCspStatuses method [Security],IX509CertificateRequestPkcs10 interface, IX509CertificateRequestPkcs10 interface [Security],GetCspStatuses method, IX509CertificateRequestPkcs10.GetCspStatuses, IX509CertificateRequestPkcs10::GetCspStatuses, XCN_AT_KEYEXCHANGE, XCN_AT_NONE, XCN_AT_SIGNATURE, certenroll/IX509CertificateRequestPkcs10::GetCspStatuses, security.ix509certificaterequestpkcs10_getcspstatuses_method
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
 - IX509CertificateRequestPkcs10::GetCspStatuses
 - certenroll/IX509CertificateRequestPkcs10::GetCspStatuses
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
 - IX509CertificateRequestPkcs10.GetCspStatuses
---

# IX509CertificateRequestPkcs10::GetCspStatuses


## -description

The <b>GetCspStatuses</b> method retrieves an <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatuses">ICspStatuses</a> collection that contains all provider/algorithm pairs consistent with the intended use of the private key as specified by the caller.

## -parameters

### -param KeySpec [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-x509keyspec">X509KeySpec</a> enumeration value that specifies the intended use of the key. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XCN_AT_NONE"></a><a id="xcn_at_none"></a><dl>
<dt><b>XCN_AT_NONE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Only Cryptography API: Next Generation (CNG) providers are selected.

</td>
</tr>
<tr>
<td width="40%"><a id="XCN_AT_KEYEXCHANGE"></a><a id="xcn_at_keyexchange"></a><dl>
<dt><b>XCN_AT_KEYEXCHANGE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Only CryptoAPI <a href="/windows/desktop/SecGloss/c-gly">cryptographic service providers</a> (CSPs) with encryption algorithms (including key exchange) are selected.

</td>
</tr>
<tr>
<td width="40%"><a id="XCN_AT_SIGNATURE"></a><a id="xcn_at_signature"></a><dl>
<dt><b>XCN_AT_SIGNATURE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Only CryptoAPI CSPs with signature algorithms are selected.

</td>
</tr>
</table>

### -param ppCspStatuses [out]

Address of a variable that receives a pointer to an  <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatuses">ICspStatuses</a> interface that represents the collection.

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
<dt><b>CERTSRV_E_PROPERTY_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
The private key cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_BLANK</b></dt>
</dl>
</td>
<td width="60%">
The object is not initialized.

</td>
</tr>
</table>

## -remarks

This method retrieves a collection of <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> objects. Each object represents a single provider/algorithm pair. If you specify a template when initializing the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a> request object, template attributes  such as the  <b>pKIDefaultCSPs</b> and <b>pKIDefaultKeySpec</b> affect which pairs are initially enabled. You can call the following properties on each <b>ICspStatus</b> object to retrieve information about a pair:<ul>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-icspstatus-get_cspinformation">CspInformation</a> property retrieves provider information.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-icspstatus-get_cspalgorithm">CspAlgorithm</a> property retrieves algorithm information.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-icspstatus-get_enrollmentstatus">EnrollmentStatus</a> property retrieves an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentstatus">IX509EnrollmentStatus</a> object. Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_selected">Selected</a> property on the status object to determine whether the provider/algorithm pair is enabled for this request.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-icspstatus-get_ordinal">Ordinal</a> property retrieves the position in the provider/algorithm pair collection.</li>
</ul>


The collection retrieved by this method is saved internally on the request object. Up to three collections, one for each <i>KeySpec</i> value, can be created and saved. This is done to preserve the selection state of the provider/algorithm pairs so that relevant property pages can be displayed accurately and quickly multiple times and so that the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method can identify which providers and algorithms are selected if a private key must be created. If the selection state of a provider/algorithm pair is modified, the changes are saved to the appropriate collection. Changes made to the members of one collection do not affect the members of any other collection. The collections exist as long as the PKCS #10 object continues to exist.

Assume, for example, that this method is called with the <i>KeySpec</i> parameter set to XCN_AT_SIGNATURE and that a template is used to initialize the request. The following statements will be true:<ul>
<li>A collection of <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> objects is created and saved on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a> object. The collection contains all valid provider/algorithm pairs installed on the computer.</li>
<li>Because the <i>KeySpec</i> parameter is not set to XCN_AT_NONE, the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_selected">Selected</a> property is set to SelectedNo for each Cryptography API: Next Generation (CNG) provider/algorithm pair in the collection.</li>
<li>Because the <i>KeySpec</i> parameter is not set to XCN_AT_KEYEXCHANGE, the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_selected">Selected</a> property is set to SelectedNo for each CryptoAPI CSP/algorithm pair in the collection where the algorithm can be used to encrypt data or archive a key.</li>
<li>For each provider referenced by the template or private key but not supported on the computer, a placeholder <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> object is created and added to the collection and the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_selected">Selected</a> property is set to SelectedNo.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_selected">Selected</a> property is set to SelectedYes for each CryptoAPI CSP/algorithm pair where the algorithm can be used only to sign data.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-icspstatus-get_ordinal">Ordinal</a> property is set to reflect the CSP order, if any, identified by the <b>pKIDefaultCSPs</b> template attribute. The CSPs listed first by the attribute are ordered first in the collection. This property is used during enrollment if a private key must be created. The first selected CSP/algorithm pair is used to create the key, but if the operation fails, the next selected pair is tried.</li>
<li>Calling this method again with the same <i>KeySpec</i> parameter retrieves a pointer to the existing collection created previously for that parameter value.</li>
<li>Calling this method again with a different <i>KeySpec</i> parameter will not affect the collection created for the XCN_AT_SIGNATURE <i>KeySpec</i> value. Further, changing the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_selected">Selected</a> property on any member of the new collection does not affect any member of the previous collection.</li>
</ul>


The <b>GetCspStatuses</b> method differs from the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_cspstatuses">CspStatuses</a> property by use of the <i>KeySpec</i> parameter. The method allows users to specify this value, but the property uses the value set on the private key associated with the request object.

 You must initialize the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a> object before calling this method. For more information, see any of the following methods:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializedecode">InitializeDecode</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate">InitializeFromCertificate</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromprivatekey">InitializeFromPrivateKey</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefrompublickey">InitializeFromPublicKey</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromtemplatename">InitializeFromTemplateName</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>