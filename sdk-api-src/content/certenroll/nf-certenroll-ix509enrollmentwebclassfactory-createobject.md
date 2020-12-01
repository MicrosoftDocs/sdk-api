---
UID: NF:certenroll.IX509EnrollmentWebClassFactory.CreateObject
title: IX509EnrollmentWebClassFactory::CreateObject (certenroll.h)
description: Can be used to create an object in the user context on a webpage.
helpviewer_keywords: ["CreateObject","CreateObject method [Security]","CreateObject method [Security]","IX509EnrollmentWebClassFactory interface","ICertProperties","ICertPropertyDescription","ICertPropertyFriendlyName","ICspInformation","ICspInformations","ICspStatus","IObjectId","IObjectIds","ISignerCertificate","IX500DistinguishedName","IX509CertificateRequestCmc","IX509CertificateRequestPkcs10","IX509CertificateRequestPkcs7","IX509Enrollment","IX509EnrollmentHelper","IX509EnrollmentWebClassFactory interface [Security]","CreateObject method","IX509EnrollmentWebClassFactory.CreateObject","IX509EnrollmentWebClassFactory::CreateObject","IX509Extension","IX509ExtensionEnhancedKeyUsage","IX509ExtensionKeyUsage","IX509ExtensionTemplate","IX509ExtensionTemplateName","IX509Extensions","IX509PrivateKey","certenroll/IX509EnrollmentWebClassFactory::CreateObject","security.ix509enrollmentwebclassfactory_createobject_method"]
old-location: security\ix509enrollmentwebclassfactory_createobject_method.htm
tech.root: security
ms.assetid: e865e499-1bfe-45c3-aeb3-3936f9173fd5
ms.date: 12/05/2018
ms.keywords: CreateObject, CreateObject method [Security], CreateObject method [Security],IX509EnrollmentWebClassFactory interface, ICertProperties, ICertPropertyDescription, ICertPropertyFriendlyName, ICspInformation, ICspInformations, ICspStatus, IObjectId, IObjectIds, ISignerCertificate, IX500DistinguishedName, IX509CertificateRequestCmc, IX509CertificateRequestPkcs10, IX509CertificateRequestPkcs7, IX509Enrollment, IX509EnrollmentHelper, IX509EnrollmentWebClassFactory interface [Security],CreateObject method, IX509EnrollmentWebClassFactory.CreateObject, IX509EnrollmentWebClassFactory::CreateObject, IX509Extension, IX509ExtensionEnhancedKeyUsage, IX509ExtensionKeyUsage, IX509ExtensionTemplate, IX509ExtensionTemplateName, IX509Extensions, IX509PrivateKey, certenroll/IX509EnrollmentWebClassFactory::CreateObject, security.ix509enrollmentwebclassfactory_createobject_method
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
 - IX509EnrollmentWebClassFactory::CreateObject
 - certenroll/IX509EnrollmentWebClassFactory::CreateObject
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
 - IX509EnrollmentWebClassFactory.CreateObject
---

# IX509EnrollmentWebClassFactory::CreateObject


## -description

The <b>CreateObject</b> method can be used to create an object in the user context on a webpage.

## -parameters

### -param strProgID [in]

A <b>BSTR</b> variable that contains the Prog ID. The following table shows the strings you can use for each object that can be created by using this method.

<table>
<tr>
<th>Object</th>
<th>Prog ID string</th>
</tr>
<tr>
<td width="40%"><a id="ICertProperties"></a><a id="icertproperties"></a><a id="ICERTPROPERTIES"></a><dl>
<dt><b><a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperties">ICertProperties</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CCertProperties"

</td>
</tr>
<tr>
<td width="40%"><a id="ICertPropertyDescription"></a><a id="icertpropertydescription"></a><a id="ICERTPROPERTYDESCRIPTION"></a><dl>
<dt><b><a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertydescription">ICertPropertyDescription</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CCertPropertyDescription"

</td>
</tr>
<tr>
<td width="40%"><a id="ICertPropertyFriendlyName"></a><a id="icertpropertyfriendlyname"></a><a id="ICERTPROPERTYFRIENDLYNAME"></a><dl>
<dt><b><a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyfriendlyname">ICertPropertyFriendlyName</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CCertPropertyFriendlyName"

</td>
</tr>
<tr>
<td width="40%"><a id="ICspInformation"></a><a id="icspinformation"></a><a id="ICSPINFORMATION"></a><dl>
<dt><b><a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CCspInformation"

</td>
</tr>
<tr>
<td width="40%"><a id="ICspInformations"></a><a id="icspinformations"></a><a id="ICSPINFORMATIONS"></a><dl>
<dt><b><a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformations">ICspInformations</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CCspInformations"

</td>
</tr>
<tr>
<td width="40%"><a id="ICspStatus"></a><a id="icspstatus"></a><a id="ICSPSTATUS"></a><dl>
<dt><b><a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CCspStatus"

</td>
</tr>
<tr>
<td width="40%"><a id="IObjectId"></a><a id="iobjectid"></a><a id="IOBJECTID"></a><dl>
<dt><b><a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CObjectId"

</td>
</tr>
<tr>
<td width="40%"><a id="IObjectIds"></a><a id="iobjectids"></a><a id="IOBJECTIDS"></a><dl>
<dt><b><a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectids">IObjectIds</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CObjectIds"

</td>
</tr>
<tr>
<td width="40%"><a id="ISignerCertificate"></a><a id="isignercertificate"></a><a id="ISIGNERCERTIFICATE"></a><dl>
<dt><b><a href="/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CSignerCertificate"

</td>
</tr>
<tr>
<td width="40%"><a id="IX500DistinguishedName"></a><a id="ix500distinguishedname"></a><a id="IX500DISTINGUISHEDNAME"></a><dl>
<dt><b><a href="/windows/desktop/api/certenroll/nn-certenroll-ix500distinguishedname">IX500DistinguishedName</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CX500DistinguishedName"

</td>
</tr>
<tr>
<td width="40%"><a id="IX509CertificateRequestCmc"></a><a id="ix509certificaterequestcmc"></a><a id="IX509CERTIFICATEREQUESTCMC"></a><dl>
<dt><b><a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CX509CertificateRequestCmc"

</td>
</tr>
<tr>
<td width="40%"><a id="IX509CertificateRequestPkcs10"></a><a id="ix509certificaterequestpkcs10"></a><a id="IX509CERTIFICATEREQUESTPKCS10"></a><dl>
<dt><b><a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CX509CertificateRequestPkcs10"

</td>
</tr>
<tr>
<td width="40%"><a id="IX509CertificateRequestPkcs7"></a><a id="ix509certificaterequestpkcs7"></a><a id="IX509CERTIFICATEREQUESTPKCS7"></a><dl>
<dt><b><a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CX509CertificateRequestPkcs7"

</td>
</tr>
<tr>
<td width="40%"><a id="IX509Enrollment"></a><a id="ix509enrollment"></a><a id="IX509ENROLLMENT"></a><dl>
<dt><b><a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CX509Enrollment"

</td>
</tr>
<tr>
<td width="40%"><a id="IX509EnrollmentHelper"></a><a id="ix509enrollmenthelper"></a><a id="IX509ENROLLMENTHELPER"></a><dl>
<dt><b><a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmenthelper">IX509EnrollmentHelper</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CX509EnrollmentHelper"

</td>
</tr>
<tr>
<td width="40%"><a id="IX509Extension"></a><a id="ix509extension"></a><a id="IX509EXTENSION"></a><dl>
<dt><b><a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CX509Extension"

</td>
</tr>
<tr>
<td width="40%"><a id="IX509ExtensionEnhancedKeyUsage"></a><a id="ix509extensionenhancedkeyusage"></a><a id="IX509EXTENSIONENHANCEDKEYUSAGE"></a><dl>
<dt><b><a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionenhancedkeyusage">IX509ExtensionEnhancedKeyUsage</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CX509ExtensionEnhancedKeyUsage"

</td>
</tr>
<tr>
<td width="40%"><a id="IX509ExtensionKeyUsage"></a><a id="ix509extensionkeyusage"></a><a id="IX509EXTENSIONKEYUSAGE"></a><dl>
<dt><b><a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionkeyusage">IX509ExtensionKeyUsage</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CX509ExtensionKeyUsage"

</td>
</tr>
<tr>
<td width="40%"><a id="IX509Extensions"></a><a id="ix509extensions"></a><a id="IX509EXTENSIONS"></a><dl>
<dt><b><a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CX509Extensions"

</td>
</tr>
<tr>
<td width="40%"><a id="IX509ExtensionTemplate"></a><a id="ix509extensiontemplate"></a><a id="IX509EXTENSIONTEMPLATE"></a><dl>
<dt><b><a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensiontemplate">IX509ExtensionTemplate</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CX509ExtensionTemplate"

</td>
</tr>
<tr>
<td width="40%"><a id="IX509ExtensionTemplateName"></a><a id="ix509extensiontemplatename"></a><a id="IX509EXTENSIONTEMPLATENAME"></a><dl>
<dt><b><a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensiontemplatename">IX509ExtensionTemplateName</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CX509ExtensionTemplateName"

</td>
</tr>
<tr>
<td width="40%"><a id="IX509PrivateKey"></a><a id="ix509privatekey"></a><a id="IX509PRIVATEKEY"></a><dl>
<dt><b><a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CX509PrivateKey"

</td>
</tr>
</table>

### -param ppIUnknown [out]

Address of a variable that receives a pointer to an  <b>IUnknown</b> interface that represents the created object.

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
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The Prog ID specified represents an object that cannot be created by using this method.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentwebclassfactory">IX509EnrollmentWebClassFactory</a>