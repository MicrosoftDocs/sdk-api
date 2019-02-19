---
UID: NF:msi.MsiSourceListAddSourceW
title: MsiSourceListAddSourceW function
author: windows-sdk-content
description: Adds to the list of valid network sources that contain the specified type of sources for a product or patch in a specified user context.
old-location: setup\msisourcelistaddsource.htm
tech.root: Msi
ms.assetid: 5f01a49a-38ae-4a53-967a-38aad1aa01f4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MsiSourceListAddSource, MsiSourceListAddSource function, MsiSourceListAddSourceA, MsiSourceListAddSourceW, _msi_msisourcelistaddsource, msi/MsiSourceListAddSource, msi/MsiSourceListAddSourceA, msi/MsiSourceListAddSourceW, setup.msisourcelistaddsource
ms.topic: function
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiSourceListAddSourceW (Unicode) and MsiSourceListAddSourceA (ANSI)
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
 - MsiSourceListAddSource
 - MsiSourceListAddSourceA
 - MsiSourceListAddSourceW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MsiSourceListAddSourceW function


## -description


The 
<b>MsiSourceListAddSource</b> function adds to the list of valid network sources that contain the specified type of sources for a product or patch in a specified user context.

The number of sources in the <a href="https://msdn.microsoft.com/9dc1e195-a108-4f8f-b008-e08fc7658fc0">SOURCELIST</a> property is unlimited.


## -parameters




### -param szProduct [in]

 The <a href="https://msdn.microsoft.com/33cedd37-0343-471c-ad4b-0db5f98d5894">ProductCode</a> of the product to modify.


### -param szUserName [in]

The user name for a per-user installation. On Windows 2000 or Windows XP, the user name should always be in the format of DOMAIN\USERNAME (or MACHINENAME\USERNAME for a local user).

An empty string or <b>NULL</b> for a per-machine installation. 


### -param dwReserved [in]

Reserved for future use. This value must be set to 0. 



### -param szSource [in]

Pointer to the string specifying the source.


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The user does not have the ability to add a source.

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
The source was added.

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

Note that this function merely adds the new source  to the list of valid sources. If another source was used to install the product, the new source is not used until the current source is unavailable.



It is the responsibility of the caller to ensure that the provided source is a valid source image for the product.



If the user name is an empty string or <b>NULL</b>, the function operates on the per-machine installation of the product. In this case, if the product is installed only in the per-user state, the function returns ERROR_UNKNOWN_PRODUCT. 



If the user name is not an empty string or <b>NULL</b>, it specifies the name of the user whose product installation is modified. If the user name is the current user name, the function first attempts to modify a non-managed installation of the product. If no non-managed installation of the product can be found, the function then tries to modify a managed per-user installation of the product. If no managed or unmanaged per-user installations of the product can be found, the function returns ERROR_UNKNOWN_PRODUCT, even if the product is installed per-machine.



This function can  not modify a non-managed installation for any user besides the current user. If the user name is not an empty string or <b>NULL</b>, but is not the current user, the function only checks for a managed per-user installation of the product for the specified user. If the product is not installed as managed per-user for the specified user, the function returns ERROR_UNKNOWN_PRODUCT, even if the product is installed per-machine.




## -see-also




<a href="https://msdn.microsoft.com/1cf83f77-75a4-48c3-961e-339c76ba4306">AllowLockdownBrowse</a>



<a href="https://msdn.microsoft.com/0bbec06a-0a2b-430a-a361-317a319da615">AlwaysInstallElevated</a>



<a href="https://msdn.microsoft.com/51806a4c-4ae5-42e9-9d58-8032108164cb">DisableBrowse</a>



<a href="https://msdn.microsoft.com/20e7be9f-d9dc-4f43-86d7-b1a881126925">Installation Context</a>



<a href="https://msdn.microsoft.com/72855539-469a-4289-99cc-eae2ed89901f">LookupAccountName</a>



<a href="https://msdn.microsoft.com/33cedd37-0343-471c-ad4b-0db5f98d5894">ProductCode</a>



<a href="https://msdn.microsoft.com/9dc1e195-a108-4f8f-b008-e08fc7658fc0">SOURCELIST</a>



<a href="https://msdn.microsoft.com/3d6a0524-d5df-4d4c-b861-d4a7da95ce40">Source Resiliency</a>
 

 

