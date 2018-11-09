---
UID: NN:casetup.ICertificateEnrollmentPolicyServerSetup
title: ICertificateEnrollmentPolicyServerSetup
author: windows-sdk-content
description: The ICertificateEnrollmentPolicyServerSetup interface represents the Certificate Enrollment Policy (CEP) Web Service within Active Directory Certificate Services (ADCS).
old-location: security\icertificateenrollmentpolicyserversetup.htm
tech.root: seccrypto
ms.assetid: 8C9F33BA-5FCB-4B99-869C-FADDC37A326A
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ICertificateEnrollmentPolicyServerSetup, ICertificateEnrollmentPolicyServerSetup interface [Security], ICertificateEnrollmentPolicyServerSetup interface [Security],described, casetup/ICertificateEnrollmentPolicyServerSetup, security.icertificateenrollmentpolicyserversetup
ms.prod: windows
ms.technology: windows-sdk
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

A related interface, <a href="https://msdn.microsoft.com/en-us/library/Ff808377(v=VS.85).aspx">ICertificateEnrollmentServerSetup</a>, represents the Certificate Enrollment Web Service (CES) and enables users and computers to enroll for and renew certificates. CEP and CES work together to provide policy-based certificate enrollment.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertificateEnrollmentPolicyServerSetup</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ICertificateEnrollmentPolicyServerSetup</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Ff808372(v=VS.85).aspx">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves a <a href="https://msdn.microsoft.com/en-us/library/Ff808352(v=VS.85).aspx">CEPSetupProperty</a> enumeration value for the CEP configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff808373(v=VS.85).aspx">InitializeInstallDefaults</a>
</td>
<td align="left" width="63%">
Initializes the <b>ICertificateEnrollmentPolicyServerSetup</b> object with a default configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff808374(v=VS.85).aspx">Install</a>
</td>
<td align="left" width="63%">
Installs the CEP web service configured by this object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff808375(v=VS.85).aspx">SetProperty</a>
</td>
<td align="left" width="63%">
Specifies a <a href="https://msdn.microsoft.com/en-us/library/Ff808352(v=VS.85).aspx">CEPSetupProperty</a> enumeration value for the CEP configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff808376(v=VS.85).aspx">UnInstall</a>
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

<a href="https://msdn.microsoft.com/en-us/library/Ff808371(v=VS.85).aspx">ErrorString</a>


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




<a href="https://msdn.microsoft.com/en-us/library/Ff808377(v=VS.85).aspx">ICertificateEnrollmentServerSetup</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

