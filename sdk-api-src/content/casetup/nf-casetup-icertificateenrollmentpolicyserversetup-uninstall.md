---
UID: NF:casetup.ICertificateEnrollmentPolicyServerSetup.UnInstall
title: ICertificateEnrollmentPolicyServerSetup::UnInstall (casetup.h)
description: Removes the Certificate Enrollment Policy (CEP) Web Service.
helpviewer_keywords: ["ICertificateEnrollmentPolicyServerSetup interface [Security]","UnInstall method","ICertificateEnrollmentPolicyServerSetup.UnInstall","ICertificateEnrollmentPolicyServerSetup::UnInstall","UnInstall","UnInstall method [Security]","UnInstall method [Security]","ICertificateEnrollmentPolicyServerSetup interface","casetup/ICertificateEnrollmentPolicyServerSetup::UnInstall","security.icertificateenrollmentpolicyserversetup_uninstall"]
old-location: security\icertificateenrollmentpolicyserversetup_uninstall.htm
tech.root: security
ms.assetid: 3E53903A-B716-45E7-B0EB-0D1226291275
ms.date: 12/05/2018
ms.keywords: ICertificateEnrollmentPolicyServerSetup interface [Security],UnInstall method, ICertificateEnrollmentPolicyServerSetup.UnInstall, ICertificateEnrollmentPolicyServerSetup::UnInstall, UnInstall, UnInstall method [Security], UnInstall method [Security],ICertificateEnrollmentPolicyServerSetup interface, casetup/ICertificateEnrollmentPolicyServerSetup::UnInstall, security.icertificateenrollmentpolicyserversetup_uninstall
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
 - ICertificateEnrollmentPolicyServerSetup::UnInstall
 - casetup/ICertificateEnrollmentPolicyServerSetup::UnInstall
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
 - ICertificateEnrollmentPolicyServerSetup.UnInstall
---

# ICertificateEnrollmentPolicyServerSetup::UnInstall


## -description

The <b>UnInstall</b> method removes the Certificate Enrollment Policy (CEP) Web Service.

## -parameters

### -param pAuthKeyBasedRenewal [in, optional]

A pointer to a <b>VARIANT</b> array that contains the authentication type and the optional KeyBasedRenewal values.

You can set the following values for authentication type  in the first element of the array.


<ul>
<li>X509AuthKerberos
</li>
<li>X509AuthUserName
</li>
<li>X509AuthCertificate
</li>
</ul>The second (optional) element in the array value is <b>VARIANT_TRUE</b> for a KeyBasedRenewal CEP.

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
The user must be a local administrator.

The <a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentpolicyserversetup-get_errorstring">ErrorString</a> property value is set to "You have to be the local machine administrator in order to run this setup."

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_STATE)</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentpolicyserversetup">ICertificateEnrollmentPolicyServerSetup</a> object has been initialized. An object is initialized when you successfully call <a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentpolicyserversetup-initializeinstalldefaults">InitializeInstallDefaults</a>.

The <a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentpolicyserversetup-get_errorstring">ErrorString</a> property value is set to "The object has been initialized. You cannot call UnInstall on an initialized object."

</td>
</tr>
</table>

## -remarks

You can call this method to remove the CEP service. However, because you cannot call the <b>UnInstall</b> method on an <a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentpolicyserversetup">ICertificateEnrollmentPolicyServerSetup</a> object that has already been initialized, you must create a new <b>ICertificateEnrollmentPolicyServerSetup</b> before calling <b>UnInstall</b>.

When the <i>pAuthKeyBasedRenewal</i> parameter is NULL, this  function performs the following actions:

<ul>
<li>
Initializes Windows Management Instrumentation (WMI).

</li>
<li>Attempts to delete the %Windir%\Systemdata\Cep directory and all application subdirectories that may exist. For more information, see the <a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentpolicyserversetup-install">Install</a> Remarks section.</li>
<li>
Attempts to delete the application pool and all applications in the pool.

</li>
<li>
Attempts to update the security descriptor of the Deleted Objects container in Active Directory to deny access by the computer. For more information, see the <a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentpolicyserversetup-install">Install</a> Remarks section.

</li>
</ul>
When the <i>pAuthKeyBasedRenewal</i> parameter contains values for the authentication type and KeyBasedRenewal, this function performs the actions in the previous list but it only deletes the application that corresponds to the values set in <i>pAuthKeyBasedRenewal</i> and leaves other applications in place.

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentpolicyserversetup">ICertificateEnrollmentPolicyServerSetup</a>



<a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentpolicyserversetup-initializeinstalldefaults">InitializeInstallDefaults</a>



<a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentpolicyserversetup-install">Install</a>