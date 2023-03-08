---
UID: NN:certenroll.IX509EnrollmentWebClassFactory
title: IX509EnrollmentWebClassFactory (certenroll.h)
description: Can be used to create any of the following objects on a webpage.
helpviewer_keywords: ["IX509EnrollmentWebClassFactory","IX509EnrollmentWebClassFactory interface [Security]","IX509EnrollmentWebClassFactory interface [Security]","described","certenroll/IX509EnrollmentWebClassFactory","security.ix509enrollmentwebclassfactory"]
old-location: security\ix509enrollmentwebclassfactory.htm
tech.root: security
ms.assetid: f779c197-8467-481a-abf5-d3fd3ac90ba7
ms.date: 12/05/2018
ms.keywords: IX509EnrollmentWebClassFactory, IX509EnrollmentWebClassFactory interface [Security], IX509EnrollmentWebClassFactory interface [Security],described, certenroll/IX509EnrollmentWebClassFactory, security.ix509enrollmentwebclassfactory
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
 - IX509EnrollmentWebClassFactory
 - certenroll/IX509EnrollmentWebClassFactory
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
 - IX509EnrollmentWebClassFactory
---

# IX509EnrollmentWebClassFactory interface


## -description

The <b>IX509EnrollmentWebClassFactory</b> interface can be used to create any of the following objects on a webpage. These objects cannot be created directly inside a script. Only the <b>IX509EnrollmentWebClassFactory</b> can be directly created. You must call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentwebclassfactory-createobject">CreateObject</a> method for each of the following:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperties">ICertProperties</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertydescription">ICertPropertyDescription</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyfriendlyname">ICertPropertyFriendlyName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformations">ICspInformations</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectids">IObjectIds</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix500distinguishedname">IX500DistinguishedName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionenhancedkeyusage">IX509ExtensionEnhancedKeyUsage</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionkeyusage">IX509ExtensionKeyUsage</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensiontemplate">IX509ExtensionTemplate</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensiontemplatename">IX509ExtensionTemplateName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>
</li>
</ul>


The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentwebclassfactory-createobject">CreateObject</a> method suppresses most of the dialog boxes that Internet Explorer displays in zones with limited trust.

## -inheritance

The <b>IX509EnrollmentWebClassFactory</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IX509EnrollmentWebClassFactory</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
