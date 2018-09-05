---
UID: NF:certenroll.IX509EnrollmentWebClassFactory.CreateObject
title: IX509EnrollmentWebClassFactory::CreateObject
author: windows-sdk-content
description: Can be used to create an object in the user context on a webpage.
old-location: security\ix509enrollmentwebclassfactory_createobject_method.htm
old-project: SecCertEnroll
ms.assetid: e865e499-1bfe-45c3-aeb3-3936f9173fd5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CreateObject, CreateObject method [Security], CreateObject method [Security],IX509EnrollmentWebClassFactory interface, ICertProperties, ICertPropertyDescription, ICertPropertyFriendlyName, ICspInformation, ICspInformations, ICspStatus, IObjectId, IObjectIds, ISignerCertificate, IX500DistinguishedName, IX509CertificateRequestCmc, IX509CertificateRequestPkcs10, IX509CertificateRequestPkcs7, IX509Enrollment, IX509EnrollmentHelper, IX509EnrollmentWebClassFactory interface [Security],CreateObject method, IX509EnrollmentWebClassFactory.CreateObject, IX509EnrollmentWebClassFactory::CreateObject, IX509Extension, IX509ExtensionEnhancedKeyUsage, IX509ExtensionKeyUsage, IX509ExtensionTemplate, IX509ExtensionTemplateName, IX509Extensions, IX509PrivateKey, certenroll/IX509EnrollmentWebClassFactory::CreateObject, security.ix509enrollmentwebclassfactory_createobject_method
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509EnrollmentWebClassFactory.CreateObject
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
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
<dt><b><a href="https://msdn.microsoft.com/b830c0af-0a38-419d-8a33-8e3626c4e8f1">ICertProperties</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CCertProperties"

</td>
</tr>
<tr>
<td width="40%"><a id="ICertPropertyDescription"></a><a id="icertpropertydescription"></a><a id="ICERTPROPERTYDESCRIPTION"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/229e8ce9-fe18-45f4-8f91-cd741052a134">ICertPropertyDescription</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CCertPropertyDescription"

</td>
</tr>
<tr>
<td width="40%"><a id="ICertPropertyFriendlyName"></a><a id="icertpropertyfriendlyname"></a><a id="ICERTPROPERTYFRIENDLYNAME"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/d2bfe2f2-423e-4620-8933-bbae4f98c62a">ICertPropertyFriendlyName</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CCertPropertyFriendlyName"

</td>
</tr>
<tr>
<td width="40%"><a id="ICspInformation"></a><a id="icspinformation"></a><a id="ICSPINFORMATION"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CCspInformation"

</td>
</tr>
<tr>
<td width="40%"><a id="ICspInformations"></a><a id="icspinformations"></a><a id="ICSPINFORMATIONS"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/8141023c-c162-46d6-9c37-e227ce1c8761">ICspInformations</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CCspInformations"

</td>
</tr>
<tr>
<td width="40%"><a id="ICspStatus"></a><a id="icspstatus"></a><a id="ICSPSTATUS"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CCspStatus"

</td>
</tr>
<tr>
<td width="40%"><a id="IObjectId"></a><a id="iobjectid"></a><a id="IOBJECTID"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CObjectId"

</td>
</tr>
<tr>
<td width="40%"><a id="IObjectIds"></a><a id="iobjectids"></a><a id="IOBJECTIDS"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/f376a33e-005b-4810-9a26-b642236ff7af">IObjectIds</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CObjectIds"

</td>
</tr>
<tr>
<td width="40%"><a id="ISignerCertificate"></a><a id="isignercertificate"></a><a id="ISIGNERCERTIFICATE"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CSignerCertificate"

</td>
</tr>
<tr>
<td width="40%"><a id="IX500DistinguishedName"></a><a id="ix500distinguishedname"></a><a id="IX500DISTINGUISHEDNAME"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/49f176d9-33f6-4bc1-992c-c613279b0969">IX500DistinguishedName</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CX500DistinguishedName"

</td>
</tr>
<tr>
<td width="40%"><a id="IX509CertificateRequestCmc"></a><a id="ix509certificaterequestcmc"></a><a id="IX509CERTIFICATEREQUESTCMC"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CX509CertificateRequestCmc"

</td>
</tr>
<tr>
<td width="40%"><a id="IX509CertificateRequestPkcs10"></a><a id="ix509certificaterequestpkcs10"></a><a id="IX509CERTIFICATEREQUESTPKCS10"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CX509CertificateRequestPkcs10"

</td>
</tr>
<tr>
<td width="40%"><a id="IX509CertificateRequestPkcs7"></a><a id="ix509certificaterequestpkcs7"></a><a id="IX509CERTIFICATEREQUESTPKCS7"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CX509CertificateRequestPkcs7"

</td>
</tr>
<tr>
<td width="40%"><a id="IX509Enrollment"></a><a id="ix509enrollment"></a><a id="IX509ENROLLMENT"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CX509Enrollment"

</td>
</tr>
<tr>
<td width="40%"><a id="IX509EnrollmentHelper"></a><a id="ix509enrollmenthelper"></a><a id="IX509ENROLLMENTHELPER"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/19124591-be1a-401e-9b83-c640d00de34a">IX509EnrollmentHelper</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CX509EnrollmentHelper"

</td>
</tr>
<tr>
<td width="40%"><a id="IX509Extension"></a><a id="ix509extension"></a><a id="IX509EXTENSION"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/f04e3f63-c826-4401-a1c8-b2614e0dc374">IX509Extension</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CX509Extension"

</td>
</tr>
<tr>
<td width="40%"><a id="IX509ExtensionEnhancedKeyUsage"></a><a id="ix509extensionenhancedkeyusage"></a><a id="IX509EXTENSIONENHANCEDKEYUSAGE"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/0b9606d0-351c-4d2d-b876-545a9c2cf916">IX509ExtensionEnhancedKeyUsage</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CX509ExtensionEnhancedKeyUsage"

</td>
</tr>
<tr>
<td width="40%"><a id="IX509ExtensionKeyUsage"></a><a id="ix509extensionkeyusage"></a><a id="IX509EXTENSIONKEYUSAGE"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/4325e6aa-99bb-4c9a-9b19-c5352ebf27b9">IX509ExtensionKeyUsage</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CX509ExtensionKeyUsage"

</td>
</tr>
<tr>
<td width="40%"><a id="IX509Extensions"></a><a id="ix509extensions"></a><a id="IX509EXTENSIONS"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CX509Extensions"

</td>
</tr>
<tr>
<td width="40%"><a id="IX509ExtensionTemplate"></a><a id="ix509extensiontemplate"></a><a id="IX509EXTENSIONTEMPLATE"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/2ac24ee9-f31f-4501-a4f0-321580ec2fa9">IX509ExtensionTemplate</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CX509ExtensionTemplate"

</td>
</tr>
<tr>
<td width="40%"><a id="IX509ExtensionTemplateName"></a><a id="ix509extensiontemplatename"></a><a id="IX509EXTENSIONTEMPLATENAME"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/9a2d0219-6fe3-4a75-8d28-281c0b863a35">IX509ExtensionTemplateName</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
"X509Enrollment.CX509ExtensionTemplateName"

</td>
</tr>
<tr>
<td width="40%"><a id="IX509PrivateKey"></a><a id="ix509privatekey"></a><a id="IX509PRIVATEKEY"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a></b></dt>
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

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

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




<a href="https://msdn.microsoft.com/f779c197-8467-481a-abf5-d3fd3ac90ba7">IX509EnrollmentWebClassFactory</a>
 

 

