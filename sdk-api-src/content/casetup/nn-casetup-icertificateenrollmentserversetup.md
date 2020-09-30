---
UID: NN:casetup.ICertificateEnrollmentServerSetup
title: ICertificateEnrollmentServerSetup (casetup.h)
description: The ICertificateEnrollmentServerSetup interface represents the Certificate Enrollment Web Service (CES) within Active Directory Certificate Services (ADCS).
helpviewer_keywords: ["ICertificateEnrollmentServerSetup","ICertificateEnrollmentServerSetup interface [Security]","ICertificateEnrollmentServerSetup interface [Security]","described","casetup/ICertificateEnrollmentServerSetup","security.icertificateenrollmentserversetup"]
old-location: security\icertificateenrollmentserversetup.htm
tech.root: security
ms.assetid: B25DA7C4-0503-4E3B-BABC-6EFBD9EBDDAE
ms.date: 12/05/2018
ms.keywords: ICertificateEnrollmentServerSetup, ICertificateEnrollmentServerSetup interface [Security], ICertificateEnrollmentServerSetup interface [Security],described, casetup/ICertificateEnrollmentServerSetup, security.icertificateenrollmentserversetup
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertificateEnrollmentServerSetup
 - casetup/ICertificateEnrollmentServerSetup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - ICertificateEnrollmentServerSetup
---

# ICertificateEnrollmentServerSetup interface


## -description

The <b>ICertificateEnrollmentServerSetup</b> interface represents the Certificate Enrollment Web Service (CES) within Active Directory Certificate Services (ADCS). The service enables users and computers to enroll for and renew certificates under the following conditions:<ul>
<li>Computers and users can enroll, manually renew, and automatically renew certificates when joined to a domain.</li>
<li>Users can automatically renew, enroll, and manually renew when not a member of the domain or when they are temporarily outside the security boundary of the organization.</li>
<li>Computers can enroll and manually renew but cannot automatically renew when they are not a member of the domain or when they are temporarily outside the security boundary of the organization.</li>
</ul>


A related interface, <a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentpolicyserversetup">ICertificateEnrollmentPolicyServerSetup</a>, represents the Certificate Enrollment Policy (CEP) Web Service and  enables users and computers to obtain certificate enrollment policy information. CEP and CES work together to provide policy-based certificate enrollment.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertificateEnrollmentServerSetup</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertificateEnrollmentServerSetup</b> also has these types of members:
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
<a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentserversetup-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves a <a href="/windows/win32/api/casetup/ne-casetup-cessetupproperty">CESSetupProperty</a> enumeration value for the CES configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentserversetup-initializeinstalldefaults">InitializeInstallDefaults</a>
</td>
<td align="left" width="63%">
Initializes the <b>ICertificateEnrollmentServerSetup</b> object with a default configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentserversetup-install">Install</a>
</td>
<td align="left" width="63%">
Installs the service configured by the <b>ICertificateEnrollmentServerSetup</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentserversetup-setapplicationpoolcredentials">SetApplicationPoolCredentials</a>
</td>
<td align="left" width="63%">
Specifies user account information for the application pool in which CES runs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentserversetup-setproperty">SetProperty</a>
</td>
<td align="left" width="63%">
Specifies a <a href="/windows/win32/api/casetup/ne-casetup-cessetupproperty">CESSetupProperty</a> enumeration value for the CES configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentserversetup-uninstall">UnInstall</a>
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

<a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentserversetup-get_errorstring">ErrorString</a>


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

<a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentpolicyserversetup">ICertificateEnrollmentPolicyServerSetup</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>