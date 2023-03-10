---
UID: NF:casetup.ICertificateEnrollmentPolicyServerSetup.InitializeInstallDefaults
title: ICertificateEnrollmentPolicyServerSetup::InitializeInstallDefaults (casetup.h)
description: Initializes the ICertificateEnrollmentPolicyServerSetup object with a default configuration.
helpviewer_keywords: ["ICertificateEnrollmentPolicyServerSetup interface [Security]","InitializeInstallDefaults method","ICertificateEnrollmentPolicyServerSetup.InitializeInstallDefaults","ICertificateEnrollmentPolicyServerSetup::InitializeInstallDefaults","InitializeInstallDefaults","InitializeInstallDefaults method [Security]","InitializeInstallDefaults method [Security]","ICertificateEnrollmentPolicyServerSetup interface","casetup/ICertificateEnrollmentPolicyServerSetup::InitializeInstallDefaults","security.icertificateenrollmentpolicyserversetup_initializeinstalldefaults"]
old-location: security\icertificateenrollmentpolicyserversetup_initializeinstalldefaults.htm
tech.root: security
ms.assetid: C7E82D9B-DC1A-4268-8973-5D07D977451D
ms.date: 12/05/2018
ms.keywords: ICertificateEnrollmentPolicyServerSetup interface [Security],InitializeInstallDefaults method, ICertificateEnrollmentPolicyServerSetup.InitializeInstallDefaults, ICertificateEnrollmentPolicyServerSetup::InitializeInstallDefaults, InitializeInstallDefaults, InitializeInstallDefaults method [Security], InitializeInstallDefaults method [Security],ICertificateEnrollmentPolicyServerSetup interface, casetup/ICertificateEnrollmentPolicyServerSetup::InitializeInstallDefaults, security.icertificateenrollmentpolicyserversetup_initializeinstalldefaults
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
 - ICertificateEnrollmentPolicyServerSetup::InitializeInstallDefaults
 - casetup/ICertificateEnrollmentPolicyServerSetup::InitializeInstallDefaults
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
 - ICertificateEnrollmentPolicyServerSetup.InitializeInstallDefaults
---

# ICertificateEnrollmentPolicyServerSetup::InitializeInstallDefaults


## -description

The <b>InitializeInstallDefaults</b> method initializes the <a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentpolicyserversetup">ICertificateEnrollmentPolicyServerSetup</a> object with a default configuration.



## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
A user must be an administrator of the domain root or the enterprise. A computer must be joined to the domain.

If the user is not a domain root or enterprise administrator, the <a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentpolicyserversetup-get_errorstring">ErrorString</a> property is set to:

"You must be a member of the Enterprise Admins group to run Setup."

If the computer is not joined to the domain, the <a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentpolicyserversetup-get_errorstring">ErrorString</a> property is set to:

"The Certificate Enrollment Web Service or Certificate Enrollment Policy Web Service cannot be installed on a computer that is not a member of a domain."

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_STATE)</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentpolicyserversetup">ICertificateEnrollmentPolicyServerSetup</a> object has already been initialized. The <a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentpolicyserversetup-get_errorstring">ErrorString</a> property is set to:

"The setup object has already been initialized. This object cannot be initialized more than once."

</td>
</tr>
</table>

## -remarks

This method performs the following actions:

<ul>
<li>
Sets the default authentication procedure to Kerberos. You can call <a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentpolicyserversetup-setproperty">SetProperty</a> to change the authentication method.

</li>
<li>
Sets the default URL to https://<i>computerDNSname</i>/ADPolicyProvider_CEP_Kerberos/service.svc/CEP.

</li>
<li>
Checks to determine whether  the  CEP service is installed on a computer running Windows Server 2008 R2.


<div class="alert"><b>Note</b>  If this check fails, the method sets the <a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentserversetup-get_errorstring">ErrorString</a> property to "The Certificate Enrollment Web Service or Certificate Enrollment Policy Web Service must be installed on a member server in an Active Directory forest in which the Windows Server 2008 R2 version of ADPrep /forestprep has been successfully run."</div>
<div> </div>


</li>
</ul>
You must call the <b>InitializeInstallDefaults</b> method before calling any method other than <a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentpolicyserversetup-uninstall">UnInstall</a>. Call the <a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentpolicyserversetup-install">Install</a> method to install the configured CEP service. Call the <b>UnInstall</b> method on a new <a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentpolicyserversetup">ICertificateEnrollmentPolicyServerSetup</a> object to remove the service.

## -see-also

<a href="/windows/win32/api/casetup/ne-casetup-cepsetupproperty">CEPSetupProperty</a>



<a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentpolicyserversetup">ICertificateEnrollmentPolicyServerSetup</a>



<a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentpolicyserversetup-setproperty">SetProperty</a>
