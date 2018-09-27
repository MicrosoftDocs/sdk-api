---
UID: NF:msi.MsiSourceListClearAllW
title: MsiSourceListClearAllW function
author: windows-sdk-content
description: The MsiSourceListClearAll function removes all network sources from the source list of a patch or product in a specified context. For more information, see Source Resiliency.
old-location: setup\msisourcelistclearall.htm
tech.root: msi
ms.assetid: e46d222d-f788-4b68-b7ff-a72261e1066b
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: MsiSourceListClearAll, MsiSourceListClearAll function, MsiSourceListClearAllA, MsiSourceListClearAllW, _msi_msisourcelistclearall, msi/MsiSourceListClearAll, msi/MsiSourceListClearAllA, msi/MsiSourceListClearAllW, setup.msisourcelistclearall
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
req.unicode-ansi: MsiSourceListClearAllW (Unicode) and MsiSourceListClearAllA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiSourceListClearAll
 - MsiSourceListClearAllA
 - MsiSourceListClearAllW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MsiSourceListClearAllW function


## -description


The 
<b>MsiSourceListClearAll</b> function removes all network sources from the source list of a patch or product in a specified context. For more information, see 
<a href="https://msdn.microsoft.com/3d6a0524-d5df-4d4c-b861-d4a7da95ce40">Source Resiliency</a>.
		


## -parameters




### -param szProduct [in]

 The <a href="https://msdn.microsoft.com/33cedd37-0343-471c-ad4b-0db5f98d5894">ProductCode</a> of the product to modify.


### -param szUserName [in]

The user name for a per-user installation. The user name should always be in the format of DOMAIN\USERNAME (or MACHINENAME\USERNAME for a local user).  


An empty string or <b>NULL</b> for a per-machine installation. 


### -param dwReserved [in]

Reserved for future use. This value must be set to 0. 



## -returns



The <b>MsiSourceListClearAll</b> function returns the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The user does not have the ability to clear the source list for this product.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_CONFIGURATION</b></dt>
</dl>
</td>
<td width="60%">
The configuration data is corrupt.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_USERNAME</b></dt>
</dl>
</td>
<td width="60%">
Could not resolve the user name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FUNCTION_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The function did not succeed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_SERVICE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
Could not access installer service.

</td>
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
<dt><b>ERROR_UNKNOWN_PRODUCT</b></dt>
</dl>
</td>
<td width="60%">
The specified product is unknown.

</td>
</tr>
</table>
 




## -remarks



An administrator can modify per-machine installations, their own per-user non-managed installations, and the per-user managed installations for any user. A non-administrator can only modify per-machine installations and their own (managed or non-managed)per-user installations.  Users can be enabled to browse for sources by setting policy. For more information, see the <a href="https://msdn.microsoft.com/51806a4c-4ae5-42e9-9d58-8032108164cb">DisableBrowse</a>, <a href="https://msdn.microsoft.com/1cf83f77-75a4-48c3-961e-339c76ba4306">AllowLockdownBrowse</a>, and <a href="https://msdn.microsoft.com/0bbec06a-0a2b-430a-a361-317a319da615">AlwaysInstallElevated</a> policies.

If a network source is the current source for the product, this function forces the installer to search the source list for a valid source the next time a source is needed. If the current source is media or a URL source, it is still valid after this call and the source list is not searched unless <a href="https://msdn.microsoft.com/b58747bf-65db-4563-b09a-0b05d2cf62ea">MsiSourceListForceResolution</a> is also called.


If the user name is an empty string or <b>NULL</b>, the function operates on the per-machine installation of the product. In this case, if the product is installed as per-user only, the function returns ERROR_UNKNOWN_PRODUCT. 



If the user name is not an empty string or <b>NULL</b>, it specifies the name of the user whose product installation is modified. If the user name is the current user name, the function first attempts to modify a non-managed installation of the product. If no non-managed installation of the product can be found, the function then tries to modify a managed per-user installation of the product. If no managed or unmanaged per-user installations of the product can be found, the function returns ERROR_UNKNOWN_PRODUCT, even if the product is installed per-machine.

This function cannot modify a non-managed installation for any user besides the current user. If the user name is not an empty string or <b>NULL</b>, but is not the current user, the function only checks for a managed per-user installation of the product for the specified user. If the product is not installed as managed per-user for the specified user, the function returns ERROR_UNKNOWN_PRODUCT, even if the product is installed per-machine.




## -see-also




<a href="https://msdn.microsoft.com/1cf83f77-75a4-48c3-961e-339c76ba4306">AllowLockdownBrowse</a>



<a href="https://msdn.microsoft.com/0bbec06a-0a2b-430a-a361-317a319da615">AlwaysInstallElevated</a>



<a href="https://msdn.microsoft.com/51806a4c-4ae5-42e9-9d58-8032108164cb">DisableBrowse</a>



<a href="https://msdn.microsoft.com/20e7be9f-d9dc-4f43-86d7-b1a881126925">Installation Context</a>



<a href="https://msdn.microsoft.com/72855539-469a-4289-99cc-eae2ed89901f">LookupAccountName</a>



<a href="https://msdn.microsoft.com/b58747bf-65db-4563-b09a-0b05d2cf62ea">MsiSourceListForceResolution</a>



<a href="https://msdn.microsoft.com/33cedd37-0343-471c-ad4b-0db5f98d5894">ProductCode</a>



<a href="https://msdn.microsoft.com/3d6a0524-d5df-4d4c-b861-d4a7da95ce40">Source Resiliency</a>
 

 

