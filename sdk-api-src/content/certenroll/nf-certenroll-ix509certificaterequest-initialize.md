---
UID: NF:certenroll.IX509CertificateRequest.Initialize
title: IX509CertificateRequest::Initialize (certenroll.h)
description: Initializes the request object for a user or a computer.
helpviewer_keywords: ["ContextAdministratorForceMachine","ContextMachine","ContextUser","IX509CertificateRequest interface [Security]","Initialize method","IX509CertificateRequest.Initialize","IX509CertificateRequest::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","IX509CertificateRequest interface","certenroll/IX509CertificateRequest::Initialize","security.ix509certificaterequest_initialize_method"]
old-location: security\ix509certificaterequest_initialize_method.htm
tech.root: security
ms.assetid: be0e2cda-5481-49ab-9a12-6dc52981fd24
ms.date: 12/05/2018
ms.keywords: ContextAdministratorForceMachine, ContextMachine, ContextUser, IX509CertificateRequest interface [Security],Initialize method, IX509CertificateRequest.Initialize, IX509CertificateRequest::Initialize, Initialize, Initialize method [Security], Initialize method [Security],IX509CertificateRequest interface, certenroll/IX509CertificateRequest::Initialize, security.ix509certificaterequest_initialize_method
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
 - IX509CertificateRequest::Initialize
 - certenroll/IX509CertificateRequest::Initialize
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
 - IX509CertificateRequest.Initialize
---

# IX509CertificateRequest::Initialize


## -description

The <b>Initialize</b> method initializes the request object for a user or a computer.

## -parameters

### -param Context [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-x509certificateenrollmentcontext">X509CertificateEnrollmentContext</a> enumeration value that specifies whether the certificate is intended for an end user, a computer, or an administrator acting on behalf of a computer. This can be one of the following values.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></dt>
</dl>
</td>
<td width="60%">
The object is already initialized.

</td>
</tr>
</table>

## -remarks

The  <b>Initialize</b> method initializes various objects depending on the type of certificate request being created. If you call this method from an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a> object, a private key object is created and the following objects are initialized:<ul>
<li>An empty <a href="/windows/desktop/api/certenroll/nn-certenroll-icryptattributes">ICryptAttributes</a> collection.</li>
<li>An empty <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection.</li>
<li>An <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectids">IObjectIds</a> collection that contains the default critical extension object identifiers, XCN_OID_KEY_USAGE and XCN_OID_BASIC_CONSTRAINTS2. This collection can be retrieved by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_criticalextensions">CriticalExtensions</a> property.</li>
<li>An empty <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectids">IObjectIds</a> collection for the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_suppressoids">SuppressOids</a> property.</li>
<li>An <a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformations">ICspInformations</a> object that contains the values you specified in the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_cspinformations">CSPInformations</a> property or a collection of all providers installed on the computer. This collection is used to create a private key.</li>
</ul>


If you call this method from an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a> object, an inner PKCS #10 request is created as above and the following objects are initialized:<ul>
<li>An empty <a href="/windows/desktop/api/certenroll/nn-certenroll-icryptattributes">ICryptAttributes</a> collection.</li>
<li>An empty <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509namevaluepairs">IX509NameValuePairs</a> collection.</li>
<li>An empty <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection.</li>
<li>An <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectids">IObjectIds</a> collection that contains the default critical extension object identifiers, XCN_OID_KEY_USAGE and XCN_OID_BASIC_CONSTRAINTS2. This collection can be retrieved by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-get_criticalextensions">CriticalExtensions</a> property.</li>
<li>An empty IObjectIds collection for the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-get_suppressoids">SuppressOids</a> property.</li>
<li>An empty <a href="/windows/desktop/api/certenroll/nn-certenroll-isignercertificates">ISignerCertificates</a> collection.</li>
</ul>


If you call this method from an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a> object, an inner PKCS #10 request is created as above.

The following properties can be called before you call this method. <ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_parentwindow">ParentWindow</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_silent">Silent</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_uicontextmessage">UIContextMessage</a>
</li>
</ul>


You must call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_cspinformations">CSPInformations</a> property before calling this method if you want to specify an <a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformations">ICspInformations</a> collection.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcertificate">IX509CertificateRequestCertificate</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a>