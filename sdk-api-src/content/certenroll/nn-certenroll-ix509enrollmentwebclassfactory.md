---
UID: NN:certenroll.IX509EnrollmentWebClassFactory
title: IX509EnrollmentWebClassFactory (certenroll.h)
author: windows-sdk-content
description: Can be used to create any of the following objects on a webpage.
old-location: security\ix509enrollmentwebclassfactory.htm
tech.root: seccertenroll
ms.assetid: f779c197-8467-481a-abf5-d3fd3ac90ba7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IX509EnrollmentWebClassFactory, IX509EnrollmentWebClassFactory interface [Security], IX509EnrollmentWebClassFactory interface [Security],described, certenroll/IX509EnrollmentWebClassFactory, security.ix509enrollmentwebclassfactory
ms.topic: interface
f1_keywords: 
 - "certenroll/IX509EnrollmentWebClassFactory"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509EnrollmentWebClassFactory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509EnrollmentWebClassFactory interface


## -description


The <b>IX509EnrollmentWebClassFactory</b> interface can be used to create any of the following objects on a webpage. These objects cannot be created directly inside a script. Only the <b>IX509EnrollmentWebClassFactory</b> can be directly created. You must call the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentwebclassfactory-createobject">CreateObject</a> method for each of the following:<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertproperties">ICertProperties</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertpropertydescription">ICertPropertyDescription</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertpropertyfriendlyname">ICertPropertyFriendlyName</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspinformations">ICspInformations</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-iobjectids">IObjectIds</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix500distinguishedname">IX500DistinguishedName</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensionenhancedkeyusage">IX509ExtensionEnhancedKeyUsage</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensionkeyusage">IX509ExtensionKeyUsage</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensiontemplate">IX509ExtensionTemplate</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensiontemplatename">IX509ExtensionTemplateName</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>
</li>
</ul>


The <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentwebclassfactory-createobject">CreateObject</a> method suppresses most of the dialog boxes that Internet Explorer displays in zones with limited trust.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509EnrollmentWebClassFactory</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IX509EnrollmentWebClassFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IX509EnrollmentWebClassFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentwebclassfactory-createobject">CreateObject</a>
</td>
<td align="left" width="63%">
Can be used to create an object from a webpage.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

