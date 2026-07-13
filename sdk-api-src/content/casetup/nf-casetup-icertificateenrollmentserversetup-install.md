---
UID: NF:casetup.ICertificateEnrollmentServerSetup.Install
title: ICertificateEnrollmentServerSetup::Install (casetup.h)
description: Installs the Certificate Enrollment Web Service (CES) configured by the ICertificateEnrollmentServerSetup object.
helpviewer_keywords: ["ICertificateEnrollmentServerSetup interface [Security]","Install method","ICertificateEnrollmentServerSetup.Install","ICertificateEnrollmentServerSetup::Install","Install","Install method [Security]","Install method [Security]","ICertificateEnrollmentServerSetup interface","casetup/ICertificateEnrollmentServerSetup::Install","security.icertificateenrollmentserversetup_install"]
old-location: security\icertificateenrollmentserversetup_install.htm
tech.root: security
ms.assetid: 35578035-1D09-48AD-B6F5-7314C989B519
ms.date: 12/05/2018
ms.keywords: ICertificateEnrollmentServerSetup interface [Security],Install method, ICertificateEnrollmentServerSetup.Install, ICertificateEnrollmentServerSetup::Install, Install, Install method [Security], Install method [Security],ICertificateEnrollmentServerSetup interface, casetup/ICertificateEnrollmentServerSetup::Install, security.icertificateenrollmentserversetup_install
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
 - ICertificateEnrollmentServerSetup::Install
 - casetup/ICertificateEnrollmentServerSetup::Install
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
 - ICertificateEnrollmentServerSetup.Install
---

# ICertificateEnrollmentServerSetup::Install


## -description

The <b>Install</b> method installs the Certificate Enrollment Web Service (CES) configured by the <a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentserversetup">ICertificateEnrollmentServerSetup</a> object.



## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The name specified for the event tracing directory or the application directory already existed but represented a file rather than a directory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_EXISTS)</b></dt>
</dl>
</td>
<td width="60%">
The CES application already exists. For more information, see Remarks

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_STATE)</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentserversetup">ICertificateEnrollmentServerSetup</a> object has not been initialized.

The <a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentserversetup-get_errorstring">ErrorString</a> property value is set to "The setup object has not been initialized. Please initialize the setup object with the InitializeInstallDefaults method."

</td>
</tr>
</table>

## -remarks

This function performs the following actions:

<ul>
<li>
Initializes Windows Management Instrumentation (WMI).

</li>
<li>
Validates the CES configuration by verifying that an application with the same name does not already exist.  The application name is part of the CES URL where the URL is of the form "https://<i>computerDNSname</i>/<i>SanitizedCAShortName</i>_ces_<i>AuthenticationType</i>/service.svc/ces". The application name consists of "<i>SanitizedCAShortName</i>_ces_<i>AuthenticationType</i>" where <i>AuthenticationType</i> can be one of the following:<ul>
<li>kerberos</li>
<li>usernamepassword</li>
<li>certificate</li>
</ul>
<div class="alert"><b>Note</b>  If an application with the same name exists, the <a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentserversetup-get_errorstring">ErrorString</a> property is set to "Setup could not add this role service because it already exists in the default website. Please remove the existing role service or select a different certification authority (CA) or authentication type."</div>
<div> </div>


</li>
<li>
Creates the %windir%\systemdata\ces&#92;<i>SanitizedCAShortName</i>_ces_<i>AuthenticationType</i> application directory. <div class="alert"><b>Note</b>  This method does not return an error if the name specified already exists as a directory, but if the specified name exists as a file or if some other error occurred, the method returns a failure <b>HRESULT</b> and sets the <a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentserversetup-get_errorstring">ErrorString</a> property to "Failed to create the directory %1."</div>
<div> </div>


</li>
<li>
Creates the %windir%\systemdata\ces&#92;<i>SanitizedCAShortName</i>_ces_<i>AuthenticationType</i>\Traces event tracing directory.

</li>
<li>
Creates the Web.config and Service.svc files and writes them to the application directory. If the files already exist, they are overwritten.

</li>
<li>
Creates an IIS application pool. By default, the pool runs under the <b>ApplicationPoolIdentity</b> account. To use a different identity, you must manually change it after the CES role has been installed.

</li>
<li>
Creates the application in the default website.

</li>
<li>
Creates a secure (https) binding to port 443 and sets the certificate hash if one was specified during configuration.

</li>
<li>
Sets IIS authentication to anonymous if you called <a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentserversetup-setproperty">SetProperty</a> and specified  X509AuthCertificate or X509AuthUsername in the <i>pPropertyValue</i> argument. Sets authentication to Windows if you called <b>SetProperty</b> and specified  X509AuthKerberos.

</li>
<li>
Sets SSL flags depending on the type of authentication chosen during configuration. The default flags for all  authentication types are SSL (require secure channel) and SSL_128 (128-bit encryption). Additionally, if you specify  X509AuthCertificate, the SSL_REQUIRE_CERT and  SSL_NEGOTIATE_CERT flags are set.

</li>
<li>
Adds read and write access to the event tracing directory.

</li>
<li>
Updates the security descriptor of the Deleted Objects container in Active Directory to permit access by the computer and/or the application pool. This enables CES to notify the certification authority when a relevant Active Directory object is deleted. If Active Directory resides on a domain controller, both the computer and application pool are allowed to access the Deleted Objects container. If Active Directory does not reside on a domain controller, only the computer is allowed access.

<div class="alert"><b>Note</b>  If access to the Deleted Objects container fails, the method returns a failure <b>HRESULT</b> and sets the <a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentpolicyserversetup-get_errorstring">ErrorString</a> property to "Setup cannot give the Certificate Enrollment Policy Web Service account List permission on the ""Deleted Objects"" container. The web service will not be able to detect deletion of Active Directory objects such as certificate templates. To complete Setup, a member of the Domain Admins group must manually give the Certificate Enrollment Policy Web Service account List permission on the ""Deleted Objects"" container in Active Directory Domain Services (AD DS)."</div>
<div> </div>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentserversetup">ICertificateEnrollmentServerSetup</a>
