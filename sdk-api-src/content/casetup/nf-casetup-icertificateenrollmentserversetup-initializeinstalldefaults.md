---
UID: NF:casetup.ICertificateEnrollmentServerSetup.InitializeInstallDefaults
title: ICertificateEnrollmentServerSetup::InitializeInstallDefaults
author: windows-sdk-content
description: Initializes the ICertificateEnrollmentServerSetup object with a default configuration.
old-location: security\icertificateenrollmentserversetup_initializeinstalldefaults.htm
tech.root: seccrypto
ms.assetid: 2C6E8F84-56AC-4541-A778-839D5F2C764F
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ICertificateEnrollmentServerSetup interface [Security],InitializeInstallDefaults method, ICertificateEnrollmentServerSetup.InitializeInstallDefaults, ICertificateEnrollmentServerSetup::InitializeInstallDefaults, InitializeInstallDefaults, InitializeInstallDefaults method [Security], InitializeInstallDefaults method [Security],ICertificateEnrollmentServerSetup interface, casetup/ICertificateEnrollmentServerSetup::InitializeInstallDefaults, security.icertificateenrollmentserversetup_initializeinstalldefaults
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ICertificateEnrollmentServerSetup.InitializeInstallDefaults
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertificateEnrollmentServerSetup::InitializeInstallDefaults


## -description


The <b>InitializeInstallDefaults</b> method initializes the <a href="https://msdn.microsoft.com/en-us/library/Ff808377(v=VS.85).aspx">ICertificateEnrollmentServerSetup</a> object with a default configuration.


## -parameters






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

If the user is not a domain root or enterprise administrator, the <a href="https://msdn.microsoft.com/en-us/library/Ff808378(v=VS.85).aspx">ErrorString</a> property is set to:

"You must be a member of the Enterprise Admins group to run Setup."

If the computer is not joined to the domain, the <a href="https://msdn.microsoft.com/en-us/library/Ff808378(v=VS.85).aspx">ErrorString</a> property is set to:

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
The <a href="https://msdn.microsoft.com/en-us/library/Ff808377(v=VS.85).aspx">ICertificateEnrollmentServerSetup</a> object has already been initialized. The <a href="https://msdn.microsoft.com/en-us/library/Ff808378(v=VS.85).aspx">ErrorString</a> property is set to:

"The setup object has already been initialized. This object cannot be initialized more than once."

</td>
</tr>
</table>
 




## -remarks



This method performs the following actions:

<ul>
<li>
Determines whether the <a href="https://msdn.microsoft.com/en-us/library/Ff808377(v=VS.85).aspx">ICertificateEnrollmentServerSetup</a> object has already been initialized.


<div class="alert"><b>Note</b>  If this check fails, the method sets the <a href="https://msdn.microsoft.com/en-us/library/Ff808378(v=VS.85).aspx">ErrorString</a> property to "The setup object has already been initialized. This object cannot be initialized more than once."</div>
<div> </div>


</li>
<li>
Determines whether the user is an administrator of the domain root or the enterprise.


<div class="alert"><b>Note</b>  If this check fails, the method sets the <a href="https://msdn.microsoft.com/en-us/library/Ff808378(v=VS.85).aspx">ErrorString</a> property to "You must be a member of the Enterprise Admins group to run Setup."</div>
<div> </div>


</li>
<li>
Determines whether the computer is joined to the domain.


<div class="alert"><b>Note</b>  If this check fails, the method sets the <a href="https://msdn.microsoft.com/en-us/library/Ff808378(v=VS.85).aspx">ErrorString</a> property to "The Certificate Enrollment Web Service or Certificate Enrollment Policy Web Service cannot be installed on a computer that is not a member of a domain."</div>
<div> </div>


</li>
<li>Sets the default authentication procedure to Kerberos. You can call <a href="https://msdn.microsoft.com/en-us/library/Ff808383(v=VS.85).aspx">SetProperty</a> to change the authentication method. </li>
<li>
Determines whether  CES is installed on a computer running Windows Server 2008 R2.


<div class="alert"><b>Note</b>  If this check fails, the method sets the <a href="https://msdn.microsoft.com/en-us/library/Ff808378(v=VS.85).aspx">ErrorString</a> property to "The Certificate Enrollment Web Service or Certificate Enrollment Policy Web Service must be installed on a member server in an Active Directory forest in which the Windows Server 2008 R2 version of ADPrep /forestprep has been successfully run."</div>
<div> </div>


</li>
<li>Sets the default server context to the <b>ApplicationPoolIdentity</b> built-in account.</li>
<li>Sets the ENUM_CESSETUPPROP_RENEWALONLY property to <b>FALSE</b>.</li>
<li>
Sets the ENUM_CESSETUPPROP_URL property is to "https://<i>computerDNSname</i>/<i>SanitizedCAShortName</i>_CES_Kerberos/service.svc/ces" if a valid certification authority (CA) configuration exists. If a valid configuration does not exist, the ENUM_CESSETUPPROP_URL property is not set. The <i>SanitizedCAShortName</i> is the sanitized short name of the CA. For more information about sanitized names, see <a href="https://msdn.microsoft.com/en-us/library/Aa385028(v=VS.85).aspx">GetConfig</a>.


<div class="alert"><b>Note</b>  If the certification authority is a standalone CA, the <a href="https://msdn.microsoft.com/en-us/library/Ff808378(v=VS.85).aspx">ErrorString</a> property is set to "The Certificate Enrollment Web Service cannot be used with a standalone certification authority (CA). It can only be used with an enterprise CA."</div>
<div> </div>


</li>
</ul>
You must call the <b>InitializeInstallDefaults</b> method before calling any method other than <a href="https://msdn.microsoft.com/en-us/library/Ff808384(v=VS.85).aspx">UnInstall</a>. Call the <a href="https://msdn.microsoft.com/en-us/library/Ff808381(v=VS.85).aspx">Install</a> method to install the configured service. Call <b>UnInstall</b> on a new <a href="https://msdn.microsoft.com/en-us/library/Ff808377(v=VS.85).aspx">ICertificateEnrollmentServerSetup</a> object to remove the service.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff808361(v=VS.85).aspx">CESSetupProperty</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff808377(v=VS.85).aspx">ICertificateEnrollmentServerSetup</a>
 

 

