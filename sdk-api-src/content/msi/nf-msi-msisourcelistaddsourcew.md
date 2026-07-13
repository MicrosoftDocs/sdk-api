---
UID: NF:msi.MsiSourceListAddSourceW
title: MsiSourceListAddSourceW function (msi.h)
description: Adds to the list of valid network sources that contain the specified type of sources for a product or patch in a specified user context. (Unicode)
helpviewer_keywords: ["MsiSourceListAddSource", "MsiSourceListAddSource function", "MsiSourceListAddSourceW", "_msi_msisourcelistaddsource", "msi/MsiSourceListAddSource", "msi/MsiSourceListAddSourceW", "setup.msisourcelistaddsource"]
old-location: setup\msisourcelistaddsource.htm
tech.root: setup
ms.assetid: 5f01a49a-38ae-4a53-967a-38aad1aa01f4
ms.date: 12/05/2018
ms.keywords: MsiSourceListAddSource, MsiSourceListAddSource function, MsiSourceListAddSourceA, MsiSourceListAddSourceW, _msi_msisourcelistaddsource, msi/MsiSourceListAddSource, msi/MsiSourceListAddSourceA, msi/MsiSourceListAddSourceW, setup.msisourcelistaddsource
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiSourceListAddSourceW
 - msi/MsiSourceListAddSourceW
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
 - MsiSourceListAddSource
 - MsiSourceListAddSourceA
 - MsiSourceListAddSourceW
---

# MsiSourceListAddSourceW function


## -description

The 
<b>MsiSourceListAddSource</b> function adds to the list of valid network sources that contain the specified type of sources for a product or patch in a specified user context.

The number of sources in the <a href="/windows/desktop/Msi/sourcelist">SOURCELIST</a> property is unlimited.

## -parameters

### -param szProduct [in]

 The <a href="/windows/desktop/Msi/productcode">ProductCode</a> of the product to modify.

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

An administrator can modify per-machine installations, their own per-user non-managed installations, and the per-user managed installations for any user. A non-administrator can only modify per-machine installations and their own (managed or non-managed)per-user installations.  Users can be enabled to browse for sources by setting policy. For more information, see the <a href="/windows/desktop/Msi/disablebrowse">DisableBrowse</a>, <a href="/windows/desktop/Msi/allowlockdownbrowse">AllowLockdownBrowse</a>, and <a href="/windows/desktop/Msi/alwaysinstallelevated">AlwaysInstallElevated</a> policies.

Note that this function merely adds the new source  to the list of valid sources. If another source was used to install the product, the new source is not used until the current source is unavailable.



It is the responsibility of the caller to ensure that the provided source is a valid source image for the product.



If the user name is an empty string or <b>NULL</b>, the function operates on the per-machine installation of the product. In this case, if the product is installed only in the per-user state, the function returns ERROR_UNKNOWN_PRODUCT. 



If the user name is not an empty string or <b>NULL</b>, it specifies the name of the user whose product installation is modified. If the user name is the current user name, the function first attempts to modify a non-managed installation of the product. If no non-managed installation of the product can be found, the function then tries to modify a managed per-user installation of the product. If no managed or unmanaged per-user installations of the product can be found, the function returns ERROR_UNKNOWN_PRODUCT, even if the product is installed per-machine.



This function can  not modify a non-managed installation for any user besides the current user. If the user name is not an empty string or <b>NULL</b>, but is not the current user, the function only checks for a managed per-user installation of the product for the specified user. If the product is not installed as managed per-user for the specified user, the function returns ERROR_UNKNOWN_PRODUCT, even if the product is installed per-machine.





> [!NOTE]
> The msi.h header defines MsiSourceListAddSource as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/allowlockdownbrowse">AllowLockdownBrowse</a>



<a href="/windows/desktop/Msi/alwaysinstallelevated">AlwaysInstallElevated</a>



<a href="/windows/desktop/Msi/disablebrowse">DisableBrowse</a>



<a href="/windows/desktop/Msi/installation-context">Installation Context</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea">LookupAccountName</a>



<a href="/windows/desktop/Msi/productcode">ProductCode</a>



<a href="/windows/desktop/Msi/sourcelist">SOURCELIST</a>



<a href="/windows/desktop/Msi/source-resiliency">Source Resiliency</a>
