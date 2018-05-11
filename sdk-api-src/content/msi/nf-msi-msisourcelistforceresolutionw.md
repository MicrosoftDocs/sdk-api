---
UID: NF:msi.MsiSourceListForceResolutionW
title: MsiSourceListForceResolutionW function
author: windows-driver-content
description: The MsiSourceListForceResolution function forces the installer to search the source list for a valid product source the next time a source is required.
old-location: setup\msisourcelistforceresolution.htm
old-project: Msi
ms.assetid: b58747bf-65db-4563-b09a-0b05d2cf62ea
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: MsiSourceListForceResolution, MsiSourceListForceResolution function, MsiSourceListForceResolutionA, MsiSourceListForceResolutionW, _msi_msisourcelistforceresolution, msi/MsiSourceListForceResolution, msi/MsiSourceListForceResolutionA, msi/MsiSourceListForceResolutionW, setup.msisourcelistforceresolution
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
req.unicode-ansi: MsiSourceListForceResolutionW (Unicode) and MsiSourceListForceResolutionA (ANSI)
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
-	MsiSourceListForceResolution
-	MsiSourceListForceResolutionA
-	MsiSourceListForceResolutionW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# MsiSourceListForceResolutionW function


## -description



			The 
<b>MsiSourceListForceResolution</b> function forces the installer to search the source list for a valid product source the next time a source is required. For example, when the installer performs an installation or reinstallation, or when it requires the path for a component that is set to run from source.
		


## -parameters




### -param szProduct [in]

 The <a href="https://msdn.microsoft.com/33cedd37-0343-471c-ad4b-0db5f98d5894">ProductCode</a> of the product to modify.


### -param szUserName [in]

The user name for a per-user installation. The user name should always be in the format of DOMAIN\USERNAME (or MACHINENAME\USERNAME for a local user). 

An empty string or <b>NULL</b> for a per-machine installation. 


### -param dwReserved [in]

Reserved for future use. This value must be set to 0. 



## -returns




					The <b>MsiSourceListForceResolution</b> function returns the following values.

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
The caller does not have sufficient access to force resolution for the product.

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
<dt><b>ERROR_BAD_USER_NAME</b></dt>
</dl>
</td>
<td width="60%">
The specified user is not a valid user.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FUNCTION_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The function could not complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_SERVICE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The installation service could not be accessed.

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



An administrator can modify per-machine installations, their own per-user non-managed installations, and the per-user managed installations for any user. A non-administrator can only modify per-machine installations and their own (managed or non-managed) per-user installations.  

If the user name is an empty string or <b>NULL</b>, the function operates on the per-machine installation of the product. In this case, if the product is installed as per-user only, the function returns ERROR_UNKNOWN_PRODUCT. 



If the user name is not an empty string or <b>NULL</b>, it specifies the name of the user whose product installation is modified. If the user name is the current user name, the function first attempts to modify a non-managed installation of the product. If no non-managed installation of the product can be found, the function then tries to modify a managed per-user installation of the product. If no managed or unmanaged per-user installations of the product can be found, the function returns ERROR_UNKNOWN_PRODUCT, even if the product is installed per-machine.

This function can  not modify a non-managed installation for any user besides the current user. If the user name is not an empty string or <b>NULL</b>, but is not the current user, the function only checks for a managed per-user installation of the product for the specified user. If the product is not installed as managed per-user for the specified user, the function returns ERROR_UNKNOWN_PRODUCT, even if the product is installed per-machine.




## -see-also




<a href="https://msdn.microsoft.com/20e7be9f-d9dc-4f43-86d7-b1a881126925">Installation Context</a>



<a href="https://msdn.microsoft.com/72855539-469a-4289-99cc-eae2ed89901f">LookupAccountName</a>



<a href="https://msdn.microsoft.com/957fd25c-8db6-4f2e-a705-1e8c3b3de6c1">MsiGetComponentPath</a>



<a href="https://msdn.microsoft.com/3d6a0524-d5df-4d4c-b861-d4a7da95ce40">Source Resiliency</a>
 

 

