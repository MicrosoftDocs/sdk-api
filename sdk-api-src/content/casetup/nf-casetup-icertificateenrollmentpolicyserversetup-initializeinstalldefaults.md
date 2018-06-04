---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ICertificateEnrollmentPolicyServerSetup::InitializeInstallDefaults


## -description


The <b>InitializeInstallDefaults</b> method initializes the <a href="https://msdn.microsoft.com/8C9F33BA-5FCB-4B99-869C-FADDC37A326A">ICertificateEnrollmentPolicyServerSetup</a> object with a default configuration.


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

If the user is not a domain root or enterprise administrator, the <a href="https://msdn.microsoft.com/CA9103BD-96CA-4FF3-B78D-A1F1345E58D3">ErrorString</a> property is set to:

"You must be a member of the Enterprise Admins group to run Setup."

If the computer is not joined to the domain, the <a href="https://msdn.microsoft.com/CA9103BD-96CA-4FF3-B78D-A1F1345E58D3">ErrorString</a> property is set to:

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
The <a href="https://msdn.microsoft.com/8C9F33BA-5FCB-4B99-869C-FADDC37A326A">ICertificateEnrollmentPolicyServerSetup</a> object has already been initialized. The <a href="https://msdn.microsoft.com/CA9103BD-96CA-4FF3-B78D-A1F1345E58D3">ErrorString</a> property is set to:

"The setup object has already been initialized. This object cannot be initialized more than once."

</td>
</tr>
</table>
 




## -remarks



This method performs the following actions:

<ul>
<li>
Sets the default authentication procedure to Kerberos. You can call <a href="https://msdn.microsoft.com/81E20BFF-B4EC-4FA5-A881-5BDCE3FC3057">SetProperty</a> to change the authentication method.

</li>
<li>
Sets the default URL to https://<i>computerDNSname</i>/ADPolicyProvider_CEP_Kerberos/service.svc/CEP.

</li>
<li>
Checks to determine whether  the  CEP service is installed on a computer running Windows Server 2008 R2.


<div class="alert"><b>Note</b>  If this check fails, the method sets the <a href="https://msdn.microsoft.com/D4322BE8-1CED-47D0-98C2-D5D7C151DEAB">ErrorString</a> property to "The Certificate Enrollment Web Service or Certificate Enrollment Policy Web Service must be installed on a member server in an Active Directory forest in which the Windows Server 2008 R2 version of ADPrep /forestprep has been successfully run."</div>
<div> </div>


</li>
</ul>
You must call the <b>InitializeInstallDefaults</b> method before calling any method other than <a href="https://msdn.microsoft.com/library/windows/hardware/mt593237">UnInstall</a>. Call the <a href="https://msdn.microsoft.com/66572F97-CE34-4C6B-9083-269A1AE2876D">Install</a> method to install the configured CEP service. Call the <b>UnInstall</b> method on a new <a href="https://msdn.microsoft.com/8C9F33BA-5FCB-4B99-869C-FADDC37A326A">ICertificateEnrollmentPolicyServerSetup</a> object to remove the service.




## -see-also




<a href="https://msdn.microsoft.com/344701CA-089C-4152-BDA4-249728863180">CEPSetupProperty</a>



<a href="https://msdn.microsoft.com/8C9F33BA-5FCB-4B99-869C-FADDC37A326A">ICertificateEnrollmentPolicyServerSetup</a>



<a href="https://msdn.microsoft.com/81E20BFF-B4EC-4FA5-A881-5BDCE3FC3057">SetProperty</a>
 

 

