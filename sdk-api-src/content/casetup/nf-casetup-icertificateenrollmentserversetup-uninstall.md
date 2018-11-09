---
UID: NF:casetup.ICertificateEnrollmentServerSetup.UnInstall
title: ICertificateEnrollmentServerSetup::UnInstall
author: windows-sdk-content
description: Removes the Certificate Enrollment Web Service (CES).
old-location: security\icertificateenrollmentserversetup_uninstall.htm
tech.root: seccrypto
ms.assetid: 5C979627-7544-4466-9F92-224D48904DD3
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ICertificateEnrollmentServerSetup interface [Security],UnInstall method, ICertificateEnrollmentServerSetup.UnInstall, ICertificateEnrollmentServerSetup::UnInstall, UnInstall, UnInstall method [Security], UnInstall method [Security],ICertificateEnrollmentServerSetup interface, casetup/ICertificateEnrollmentServerSetup::UnInstall, security.icertificateenrollmentserversetup_uninstall
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
 - ICertificateEnrollmentServerSetup.UnInstall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertificateEnrollmentServerSetup::UnInstall


## -description


The <b>UnInstall</b> method removes the Certificate Enrollment Web Service (CES).


## -parameters




### -param pCAConfig

TBD


### -param pAuthentication

TBD




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

The <a href="https://msdn.microsoft.com/en-us/library/Ff808378(v=VS.85).aspx">ErrorString</a> property value is set to "You have to be the local machine administrator in order to run this setup."

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_STATE)</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/en-us/library/Ff808377(v=VS.85).aspx">ICertificateEnrollmentServerSetup</a> object has been initialized. An object is initialized when you successfully call <a href="https://msdn.microsoft.com/en-us/library/Ff808380(v=VS.85).aspx">InitializeInstallDefaults</a>.

The <a href="https://msdn.microsoft.com/en-us/library/Ff808378(v=VS.85).aspx">ErrorString</a> property value is set to "The object has been initialized. You cannot call UnInstall on an initialized object."

</td>
</tr>
</table>
 




## -remarks



You can call this method to remove CES. However, because you cannot call the <b>UnInstall</b> method on an <a href="https://msdn.microsoft.com/en-us/library/Ff808377(v=VS.85).aspx">ICertificateEnrollmentServerSetup</a> object that has already been initialized, you must create a new <b>ICertificateEnrollmentServerSetup</b> before calling <b>UnInstall</b>.

This method attempts to delete all CES-related  directories and the application pool. If it is unable to do so, it still returns S_OK, but you can check the  <a href="https://msdn.microsoft.com/en-us/library/Ff808378(v=VS.85).aspx">ErrorString</a> property to determine what problems the method encountered.

This function performs the following actions:

<ul>
<li>
Initializes Windows Management Instrumentation (WMI).

</li>
<li>
Attempts to delete the %windir%\systemdata\ces directory and all application subdirectories that may exist. For more information, see the <a href="https://msdn.microsoft.com/en-us/library/Ff808381(v=VS.85).aspx">Install</a> Remarks section.

</li>
<li>
Attempts to delete the application pool and all applications in the pool.

</li>
<li>
Attempts to update the security descriptor of the Deleted Objects container in Active Directory to deny access by the computer. For more information, see the <a href="https://msdn.microsoft.com/en-us/library/Ff808381(v=VS.85).aspx">Install</a> Remarks section.

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff808377(v=VS.85).aspx">ICertificateEnrollmentServerSetup</a>
 

 

