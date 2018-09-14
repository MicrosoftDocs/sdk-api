---
UID: NN:certenroll.IX509EnrollmentWebClassFactory
title: IX509EnrollmentWebClassFactory
author: windows-sdk-content
description: Can be used to create any of the following objects on a webpage.
old-location: security\ix509enrollmentwebclassfactory.htm
tech.root: seccertenroll
ms.assetid: f779c197-8467-481a-abf5-d3fd3ac90ba7
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IX509EnrollmentWebClassFactory, IX509EnrollmentWebClassFactory interface [Security], IX509EnrollmentWebClassFactory interface [Security],described, certenroll/IX509EnrollmentWebClassFactory, security.ix509enrollmentwebclassfactory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509EnrollmentWebClassFactory interface


## -description


The <b>IX509EnrollmentWebClassFactory</b> interface can be used to create any of the following objects on a webpage. These objects cannot be created directly inside a script. Only the <b>IX509EnrollmentWebClassFactory</b> can be directly created. You must call the <a href="https://msdn.microsoft.com/e865e499-1bfe-45c3-aeb3-3936f9173fd5">CreateObject</a> method for each of the following:<ul>
<li>
<a href="https://msdn.microsoft.com/b830c0af-0a38-419d-8a33-8e3626c4e8f1">ICertProperties</a>
</li>
<li>
<a href="https://msdn.microsoft.com/229e8ce9-fe18-45f4-8f91-cd741052a134">ICertPropertyDescription</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d2bfe2f2-423e-4620-8933-bbae4f98c62a">ICertPropertyFriendlyName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8141023c-c162-46d6-9c37-e227ce1c8761">ICspInformations</a>
</li>
<li>
<a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a>
</li>
<li>
<a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f376a33e-005b-4810-9a26-b642236ff7af">IObjectIds</a>
</li>
<li>
<a href="https://msdn.microsoft.com/49f176d9-33f6-4bc1-992c-c613279b0969">IX500DistinguishedName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a>
</li>
<li>
<a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f04e3f63-c826-4401-a1c8-b2614e0dc374">IX509Extension</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0b9606d0-351c-4d2d-b876-545a9c2cf916">IX509ExtensionEnhancedKeyUsage</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4325e6aa-99bb-4c9a-9b19-c5352ebf27b9">IX509ExtensionKeyUsage</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2ac24ee9-f31f-4501-a4f0-321580ec2fa9">IX509ExtensionTemplate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9a2d0219-6fe3-4a75-8d28-281c0b863a35">IX509ExtensionTemplateName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
</li>
</ul>


The <a href="https://msdn.microsoft.com/e865e499-1bfe-45c3-aeb3-3936f9173fd5">CreateObject</a> method suppresses most of the dialog boxes that Internet Explorer displays in zones with limited trust.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509EnrollmentWebClassFactory</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IX509EnrollmentWebClassFactory</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/e865e499-1bfe-45c3-aeb3-3936f9173fd5">CreateObject</a>
</td>
<td align="left" width="63%">
Can be used to create an object from a webpage.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

