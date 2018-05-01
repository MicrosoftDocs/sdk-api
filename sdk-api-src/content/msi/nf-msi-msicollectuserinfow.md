---
UID: NF:msi.MsiCollectUserInfoW
title: MsiCollectUserInfoW function
author: windows-driver-content
description: The MsiCollectUserInfo function obtains and stores the user information and product ID from an installation wizard.
old-location: setup\msicollectuserinfo.htm
old-project: Msi
ms.assetid: a8be3c24-cd5a-4da9-abe7-b0e40a87a07f
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: MsiCollectUserInfo, MsiCollectUserInfo function, MsiCollectUserInfoA, MsiCollectUserInfoW, _msi_msicollectuserinfo, msi/MsiCollectUserInfo, msi/MsiCollectUserInfoA, msi/MsiCollectUserInfoW, setup.msicollectuserinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiCollectUserInfoW (Unicode) and MsiCollectUserInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DRM_CLIENT_VERSION_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msi.dll
api_name:
-	MsiCollectUserInfo
-	MsiCollectUserInfoA
-	MsiCollectUserInfoW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# MsiCollectUserInfoW function


## -description


The 
<b>MsiCollectUserInfo</b> function obtains and stores the user information and product ID from an installation wizard.


## -parameters




### -param szProduct [in]

Specifies the product code of the product for which the user information is collected.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>An error relating to an action</b></dt>
</dl>
</td>
<td width="60%">
See 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/5cce27ff-1143-4fe6-b4bd-727581431c07">Initialization Error</a></b></dt>
</dl>
</td>
<td width="60%">
An error relating to initialization occurred.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



The 
<b>MsiCollectUserInfo</b> function is typically called by an application during the first run of the application. The application first calls 
<a href="https://msdn.microsoft.com/c05580c6-9be3-410a-aa97-be15c2980ba8">MsiGetUserInfo</a>. If that call fails, the application calls 
<b>MsiCollectUserInfo</b>. 
<b>MsiCollectUserInfo</b> opens the product's installation package and invokes a wizard sequence that collects user information. Upon completion of the sequence, user information is registered. Since this API requires an authored user interface, the user interface level should be set to full by calling 
<a href="https://msdn.microsoft.com/303c2ea9-4c8f-46d3-b587-7c50e2810c28">MsiSetInternalUI</a> as INSTALLUILEVEL_FULL.

The 
<b>MsiCollectUserInfo</b> invokes a 
<a href="https://msdn.microsoft.com/bb77296f-705a-4409-b2ca-a76bbaf7ea57">FirstRun Dialog</a>.




## -see-also




<a href="https://msdn.microsoft.com/05a16915-6b47-4d51-b62a-5a4d92b87e50">Application-Only Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>



<a href="https://msdn.microsoft.com/5cce27ff-1143-4fe6-b4bd-727581431c07">Initialization Error</a>
 

 

