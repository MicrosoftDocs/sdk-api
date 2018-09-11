---
UID: NN:certenroll.IX509EnrollmentWebClassFactory
title: IX509EnrollmentWebClassFactory
author: windows-sdk-content
description: Can be used to create any of the following objects on a webpage.
old-location: security\ix509enrollmentwebclassfactory.htm
tech.root: SecCertEnroll
ms.assetid: f779c197-8467-481a-abf5-d3fd3ac90ba7
ms.author: windowssdkdev
ms.date: 08/29/2018
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


The <b>IX509EnrollmentWebClassFactory</b> interface can be used to create any of the following objects on a webpage. These objects cannot be created directly inside a script. Only the <b>IX509EnrollmentWebClassFactory</b> can be directly created. You must call the <a href="https://msdn.microsoft.com/en-us/library/Aa965817(v=VS.85).aspx">CreateObject</a> method for each of the following:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375231(v=VS.85).aspx">ICertProperties</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375646(v=VS.85).aspx">ICertPropertyDescription</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375715(v=VS.85).aspx">ICertPropertyFriendlyName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375967(v=VS.85).aspx">ICspInformation</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375968(v=VS.85).aspx">ICspInformations</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376760(v=VS.85).aspx">ICspStatus</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376784(v=VS.85).aspx">IObjectId</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376785(v=VS.85).aspx">IObjectIds</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377051(v=VS.85).aspx">IX500DistinguishedName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377133(v=VS.85).aspx">IX509CertificateRequestCmc</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377608(v=VS.85).aspx">IX509CertificateRequestPkcs7</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377809(v=VS.85).aspx">IX509Enrollment</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378077(v=VS.85).aspx">IX509Extension</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378132(v=VS.85).aspx">IX509ExtensionEnhancedKeyUsage</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378144(v=VS.85).aspx">IX509ExtensionKeyUsage</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378174(v=VS.85).aspx">IX509Extensions</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378274(v=VS.85).aspx">IX509ExtensionTemplate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378276(v=VS.85).aspx">IX509ExtensionTemplateName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a>
</li>
</ul>


The <a href="https://msdn.microsoft.com/en-us/library/Aa965817(v=VS.85).aspx">CreateObject</a> method suppresses most of the dialog boxes that Internet Explorer displays in zones with limited trust.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509EnrollmentWebClassFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IX509EnrollmentWebClassFactory</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa965817(v=VS.85).aspx">CreateObject</a>
</td>
<td align="left" width="63%">
Can be used to create an object from a webpage.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

