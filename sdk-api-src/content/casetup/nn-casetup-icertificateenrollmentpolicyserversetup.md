---
UID: NN:casetup.ICertificateEnrollmentPolicyServerSetup
title: ICertificateEnrollmentPolicyServerSetup
author: windows-sdk-content
description: The ICertificateEnrollmentPolicyServerSetup interface represents the Certificate Enrollment Policy (CEP) Web Service within Active Directory Certificate Services (ADCS).
old-location: security\icertificateenrollmentpolicyserversetup.htm
tech.root: SecCrypto
ms.assetid: 8C9F33BA-5FCB-4B99-869C-FADDC37A326A
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICertificateEnrollmentPolicyServerSetup, ICertificateEnrollmentPolicyServerSetup interface [Security], ICertificateEnrollmentPolicyServerSetup interface [Security],described, casetup/ICertificateEnrollmentPolicyServerSetup, security.icertificateenrollmentpolicyserversetup
ms.topic: interface
req.header: casetup.h
req.include-header: 
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
req.lib: 
req.dll: Certocm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - ICertificateEnrollmentPolicyServerSetup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertificateEnrollmentPolicyServerSetup interface


## -description


The <b>ICertificateEnrollmentPolicyServerSetup</b> interface represents the Certificate Enrollment Policy (CEP) Web Service within Active Directory Certificate Services (ADCS). The service enables users and computers to obtain certificate enrollment policy information even when a  computer is not a member of the domain or if a domain-joined computer is temporarily outside the security boundary of the corporate network.

A related interface, <a href="https://msdn.microsoft.com/B25DA7C4-0503-4E3B-BABC-6EFBD9EBDDAE">ICertificateEnrollmentServerSetup</a>, represents the Certificate Enrollment Web Service (CES) and enables users and computers to enroll for and renew certificates. CEP and CES work together to provide policy-based certificate enrollment.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertificateEnrollmentPolicyServerSetup</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ICertificateEnrollmentPolicyServerSetup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICertificateEnrollmentPolicyServerSetup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52AD50BB-4146-44FC-BA32-9FC46FFE32E4">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves a <a href="https://msdn.microsoft.com/344701CA-089C-4152-BDA4-249728863180">CEPSetupProperty</a> enumeration value for the CEP configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C7E82D9B-DC1A-4268-8973-5D07D977451D">InitializeInstallDefaults</a>
</td>
<td align="left" width="63%">
Initializes the <b>ICertificateEnrollmentPolicyServerSetup</b> object with a default configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66572F97-CE34-4C6B-9083-269A1AE2876D">Install</a>
</td>
<td align="left" width="63%">
Installs the CEP web service configured by this object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81E20BFF-B4EC-4FA5-A881-5BDCE3FC3057">SetProperty</a>
</td>
<td align="left" width="63%">
Specifies a <a href="https://msdn.microsoft.com/344701CA-089C-4152-BDA4-249728863180">CEPSetupProperty</a> enumeration value for the CEP configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3E53903A-B716-45E7-B0EB-0D1226291275">UnInstall</a>
</td>
<td align="left" width="63%">
Removes the CEP web service.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertificateEnrollmentPolicyServerSetup</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/CA9103BD-96CA-4FF3-B78D-A1F1345E58D3">ErrorString</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a string that contains additional information about CEP setup failure.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/B25DA7C4-0503-4E3B-BABC-6EFBD9EBDDAE">ICertificateEnrollmentServerSetup</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

