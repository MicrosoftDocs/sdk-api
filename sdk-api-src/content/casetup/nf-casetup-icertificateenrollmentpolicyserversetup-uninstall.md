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
</ul>
The second (optional) element in the array value is <b>VARIANT_TRUE</b> for a KeyBasedRenewal CEP.



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

The <a href="https://msdn.microsoft.com/CA9103BD-96CA-4FF3-B78D-A1F1345E58D3">ErrorString</a> property value is set to "You have to be the local machine administrator in order to run this setup."

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_STATE)</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/8C9F33BA-5FCB-4B99-869C-FADDC37A326A">ICertificateEnrollmentPolicyServerSetup</a> object has been initialized. An object is initialized when you successfully call <a href="https://msdn.microsoft.com/C7E82D9B-DC1A-4268-8973-5D07D977451D">InitializeInstallDefaults</a>.

The <a href="https://msdn.microsoft.com/CA9103BD-96CA-4FF3-B78D-A1F1345E58D3">ErrorString</a> property value is set to "The object has been initialized. You cannot call UnInstall on an initialized object."

</td>
</tr>
</table>
 




## -remarks



You can call this method to remove the CEP service. However, because you cannot call the <b>UnInstall</b> method on an <a href="https://msdn.microsoft.com/8C9F33BA-5FCB-4B99-869C-FADDC37A326A">ICertificateEnrollmentPolicyServerSetup</a> object that has already been initialized, you must create a new <b>ICertificateEnrollmentPolicyServerSetup</b> before calling <b>UnInstall</b>.

When the <i>pAuthKeyBasedRenewal</i> parameter is NULL, this  function performs the following actions:

<ul>
<li>
Initializes Windows Management Instrumentation (WMI).

</li>
<li>Attempts to delete the %Windir%\Systemdata\Cep directory and all application subdirectories that may exist. For more information, see the <a href="https://msdn.microsoft.com/66572F97-CE34-4C6B-9083-269A1AE2876D">Install</a> Remarks section.</li>
<li>
Attempts to delete the application pool and all applications in the pool.

</li>
<li>
Attempts to update the security descriptor of the Deleted Objects container in Active Directory to deny access by the computer. For more information, see the <a href="https://msdn.microsoft.com/66572F97-CE34-4C6B-9083-269A1AE2876D">Install</a> Remarks section.

</li>
</ul>
When the <i>pAuthKeyBasedRenewal</i> parameter contains values for the authentication type and KeyBasedRenewal, this function performs the actions in the previous list but it only deletes the application that corresponds to the values set in <i>pAuthKeyBasedRenewal</i> and leaves other applications in place.




## -see-also




<a href="https://msdn.microsoft.com/8C9F33BA-5FCB-4B99-869C-FADDC37A326A">ICertificateEnrollmentPolicyServerSetup</a>



<a href="https://msdn.microsoft.com/C7E82D9B-DC1A-4268-8973-5D07D977451D">InitializeInstallDefaults</a>



<a href="https://msdn.microsoft.com/66572F97-CE34-4C6B-9083-269A1AE2876D">Install</a>
 

 

