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

# ICertificateEnrollmentServerSetup::UnInstall


## -description


The <b>UnInstall</b> method removes the Certificate Enrollment Web Service (CES).


## -parameters




### -param pCAConfig




### -param pAuthentication






#### - pReserved [in]

This parameter is reserved for future use.


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

The <a href="https://msdn.microsoft.com/D4322BE8-1CED-47D0-98C2-D5D7C151DEAB">ErrorString</a> property value is set to "You have to be the local machine administrator in order to run this setup."

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_STATE)</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/B25DA7C4-0503-4E3B-BABC-6EFBD9EBDDAE">ICertificateEnrollmentServerSetup</a> object has been initialized. An object is initialized when you successfully call <a href="https://msdn.microsoft.com/2C6E8F84-56AC-4541-A778-839D5F2C764F">InitializeInstallDefaults</a>.

The <a href="https://msdn.microsoft.com/D4322BE8-1CED-47D0-98C2-D5D7C151DEAB">ErrorString</a> property value is set to "The object has been initialized. You cannot call UnInstall on an initialized object."

</td>
</tr>
</table>
 




## -remarks



You can call this method to remove CES. However, because you cannot call the <b>UnInstall</b> method on an <a href="https://msdn.microsoft.com/B25DA7C4-0503-4E3B-BABC-6EFBD9EBDDAE">ICertificateEnrollmentServerSetup</a> object that has already been initialized, you must create a new <b>ICertificateEnrollmentServerSetup</b> before calling <b>UnInstall</b>.

This method attempts to delete all CES-related  directories and the application pool. If it is unable to do so, it still returns S_OK, but you can check the  <a href="https://msdn.microsoft.com/D4322BE8-1CED-47D0-98C2-D5D7C151DEAB">ErrorString</a> property to determine what problems the method encountered.

This function performs the following actions:

<ul>
<li>
Initializes Windows Management Instrumentation (WMI).

</li>
<li>
Attempts to delete the %windir%\systemdata\ces directory and all application subdirectories that may exist. For more information, see the <a href="https://msdn.microsoft.com/35578035-1D09-48AD-B6F5-7314C989B519">Install</a> Remarks section.

</li>
<li>
Attempts to delete the application pool and all applications in the pool.

</li>
<li>
Attempts to update the security descriptor of the Deleted Objects container in Active Directory to deny access by the computer. For more information, see the <a href="https://msdn.microsoft.com/35578035-1D09-48AD-B6F5-7314C989B519">Install</a> Remarks section.

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/B25DA7C4-0503-4E3B-BABC-6EFBD9EBDDAE">ICertificateEnrollmentServerSetup</a>
 

 

