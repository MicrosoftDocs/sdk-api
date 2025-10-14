---
UID: NF:certenroll.IX509CertificateRequestPkcs10.InitializeDecode
title: IX509CertificateRequestPkcs10::InitializeDecode (certenroll.h)
description: Decodes an existing signed or unsigned PKCS (IX509CertificateRequestPkcs10.InitializeDecode)
helpviewer_keywords: ["IX509CertificateRequestPkcs10 interface [Security]","InitializeDecode method","IX509CertificateRequestPkcs10.InitializeDecode","IX509CertificateRequestPkcs10::InitializeDecode","InitializeDecode","InitializeDecode method [Security]","InitializeDecode method [Security]","IX509CertificateRequestPkcs10 interface","certenroll/IX509CertificateRequestPkcs10::InitializeDecode","security.ix509certificaterequestpkcs10_initializedecode_method"]
old-location: security\ix509certificaterequestpkcs10_initializedecode_method.htm
tech.root: security
ms.assetid: 10ab62c3-9c6f-4e1b-8a86-131d08282d9c
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],InitializeDecode method, IX509CertificateRequestPkcs10.InitializeDecode, IX509CertificateRequestPkcs10::InitializeDecode, InitializeDecode, InitializeDecode method [Security], InitializeDecode method [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::InitializeDecode, security.ix509certificaterequestpkcs10_initializedecode_method
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
 - IX509CertificateRequestPkcs10::InitializeDecode
 - certenroll/IX509CertificateRequestPkcs10::InitializeDecode
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
 - IX509CertificateRequestPkcs10.InitializeDecode
---

# IX509CertificateRequestPkcs10::InitializeDecode


## -description

The <b>InitializeDecode</b> method decodes an existing signed or unsigned PKCS #10 certificate request and uses it to initialize the new PKCS #10 request object.  The existing request is contained in a byte array that has been encoded by using  <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) as defined by the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) standard. The byte array is represented by a string that is either a pure binary sequence or is Unicode encoded.

## -parameters

### -param strEncodedData [in]

A <b>BSTR</b> variable that contains the DER-encoded  request. For more information, see Remarks.

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to  the input string that contains the DER-encoded request. The default value is <b>XCN_CRYPT_STRING_BASE64</b>.

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

The <b>InitializeDecode</b> method decodes the existing PKCS #10 request and uses the information retrieved to initialize the following collections for the new request object:<ul>
<li>An empty <a href="/windows/desktop/api/certenroll/nn-certenroll-icryptattributes">ICryptAttributes</a> collection.</li>
<li>An empty <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection.</li>
<li>An empty <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectids">IObjectIds</a> collection for attribute and extension OIDs to be suppressed from the new request.</li>
</ul>


The method also:<ul>
<li>Adds the decoded extensions to the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection.</li>
<li>Adds the decoded attributes to the <a href="/windows/desktop/api/certenroll/nn-certenroll-icryptattributes">ICryptAttributes</a> collection.</li>
<li>Sets the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_criticalextensions">CriticalExtensions</a> property with the decoded critical extensions.</li>
<li>Sets the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_clientid">ClientId</a> property.</li>
<li>Sets the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_templateobjectid">TemplateObjectId</a> property.</li>
</ul>


By default, the <b>InitializeDecode</b> method assumes that the certificate request to be decoded is for an end user. Beginning with Windows 8 and Windows Server 2012, you can change this default behavior. After creating an instance of the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a> interface, call <b>InitializeDecode</b> by setting the  <i>Encoding</i> parameter to <b>XCN_CRYPT_STRING_BINARY</b> and the <i>strEncodedData</i> parameter to one of the following values:

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>L"ContextMachine"</td>
<td>The encoded certificate request is for a computer.

</td>
</tr>
<tr>
<td>L"ContextUser"</td>
<td>The encoded certificate request is for an end user.</td>
</tr>
<tr>
<td>L"ContextAdministratorForceMachine"</td>
<td>The encoded certificate is being requested by an administrator acting on the behalf of a computer.

</td>
</tr>
</table>
 

Then, call the <b>InitializeDecode</b> method again with the encoded certificate set in the <i>strEncodedData</i> argument.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>
