---
UID: NN:casetup.ICertificateEnrollmentServerSetup
title: ICertificateEnrollmentServerSetup
author: windows-sdk-content
description: The ICertificateEnrollmentServerSetup interface represents the Certificate Enrollment Web Service (CES) within Active Directory Certificate Services (ADCS).
old-location: security\icertificateenrollmentserversetup.htm
old-project: SecCrypto
ms.assetid: B25DA7C4-0503-4E3B-BABC-6EFBD9EBDDAE
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: ICertificateEnrollmentServerSetup, ICertificateEnrollmentServerSetup interface [Security], ICertificateEnrollmentServerSetup interface [Security],described, casetup/ICertificateEnrollmentServerSetup, security.icertificateenrollmentserversetup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: casetup.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Casetup.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CEPSetupProperty
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - ICertificateEnrollmentServerSetup
product: Windows
targetos: Windows
req.lib: 
req.dll: Certocm.dll
req.irql: 
---

# ICertificateEnrollmentServerSetup interface


## -description


The <b>ICertificateEnrollmentServerSetup</b> interface represents the Certificate Enrollment Web Service (CES) within Active Directory Certificate Services (ADCS). The service enables users and computers to enroll for and renew certificates under the following conditions:<ul>
<li>Computers and users can enroll, manually renew, and automatically renew certificates when joined to a domain.</li>
<li>Users can automatically renew, enroll, and manually renew when not a member of the domain or when they are temporarily outside the security boundary of the organization.</li>
<li>Computers can enroll and manually renew but cannot automatically renew when they are not a member of the domain or when they are temporarily outside the security boundary of the organization.</li>
</ul>


A related interface, <a href="https://msdn.microsoft.com/8C9F33BA-5FCB-4B99-869C-FADDC37A326A">ICertificateEnrollmentPolicyServerSetup</a>, represents the Certificate Enrollment Policy (CEP) Web Service and  enables users and computers to obtain certificate enrollment policy information. CEP and CES work together to provide policy-based certificate enrollment.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertificateEnrollmentServerSetup</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ICertificateEnrollmentServerSetup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICertificateEnrollmentServerSetup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4B380551-742C-4D36-80C9-C92F62F916BB">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves a <a href="https://msdn.microsoft.com/9FA6B249-B5B3-40AF-B175-CD5933D468B9">CESSetupProperty</a> enumeration value for the CES configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2C6E8F84-56AC-4541-A778-839D5F2C764F">InitializeInstallDefaults</a>
</td>
<td align="left" width="63%">
Initializes the <b>ICertificateEnrollmentServerSetup</b> object with a default configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35578035-1D09-48AD-B6F5-7314C989B519">Install</a>
</td>
<td align="left" width="63%">
Installs the service configured by the <b>ICertificateEnrollmentServerSetup</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E85DA115-C705-44B8-B4D4-E862634CDC41">SetApplicationPoolCredentials</a>
</td>
<td align="left" width="63%">
Specifies user account information for the application pool in which CES runs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D2E20195-D81F-4717-83D2-BF8DC1D1779B">SetProperty</a>
</td>
<td align="left" width="63%">
Specifies a <a href="https://msdn.microsoft.com/9FA6B249-B5B3-40AF-B175-CD5933D468B9">CESSetupProperty</a> enumeration value for the CES configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5C979627-7544-4466-9F92-224D48904DD3">UnInstall</a>
</td>
<td align="left" width="63%">
Removes the Certificate Enrollment Web Service.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertificateEnrollmentServerSetup</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/D4322BE8-1CED-47D0-98C2-D5D7C151DEAB">ErrorString</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves a string that contains additional information about CES setup failure.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/8C9F33BA-5FCB-4B99-869C-FADDC37A326A">ICertificateEnrollmentPolicyServerSetup</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

