---
UID: NF:msi.MsiSourceListForceResolutionW
title: MsiSourceListForceResolutionW function (msi.h)
description: The MsiSourceListForceResolution function forces the installer to search the source list for a valid product source the next time a source is required. (Unicode)
helpviewer_keywords: ["MsiSourceListForceResolution", "MsiSourceListForceResolution function", "MsiSourceListForceResolutionW", "_msi_msisourcelistforceresolution", "msi/MsiSourceListForceResolution", "msi/MsiSourceListForceResolutionW", "setup.msisourcelistforceresolution"]
old-location: setup\msisourcelistforceresolution.htm
tech.root: setup
ms.assetid: b58747bf-65db-4563-b09a-0b05d2cf62ea
ms.date: 12/05/2018
ms.keywords: MsiSourceListForceResolution, MsiSourceListForceResolution function, MsiSourceListForceResolutionA, MsiSourceListForceResolutionW, _msi_msisourcelistforceresolution, msi/MsiSourceListForceResolution, msi/MsiSourceListForceResolutionA, msi/MsiSourceListForceResolutionW, setup.msisourcelistforceresolution
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
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiSourceListForceResolutionW
 - msi/MsiSourceListForceResolutionW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiSourceListForceResolution
 - MsiSourceListForceResolutionA
 - MsiSourceListForceResolutionW
---

# MsiSourceListForceResolutionW function


## -description

The 
<b>MsiSourceListForceResolution</b> function forces the installer to search the source list for a valid product source the next time a source is required. For example, when the installer performs an installation or reinstallation, or when it requires the path for a component that is set to run from source.

## -parameters

### -param szProduct [in]

 The <a href="/windows/desktop/Msi/productcode">ProductCode</a> of the product to modify.

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





> [!NOTE]
> The msi.h header defines MsiSourceListForceResolution as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/installation-context">Installation Context</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea">LookupAccountName</a>



<a href="/windows/desktop/api/msi/nf-msi-msigetcomponentpatha">MsiGetComponentPath</a>



<a href="/windows/desktop/Msi/source-resiliency">Source Resiliency</a>
