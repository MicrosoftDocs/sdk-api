---
UID: NF:msi.MsiIsProductElevatedA
title: MsiIsProductElevatedA function (msi.h)
description: The MsiIsProductElevated function returns whether or not the product is managed. (ANSI)
helpviewer_keywords: ["MsiIsProductElevatedA", "msi/MsiIsProductElevatedA"]
old-location: setup\msiisproductelevated.htm
tech.root: setup
ms.assetid: 1bf6616c-3d5a-45c9-ab69-c0bb41b3e067
ms.date: 12/05/2018
ms.keywords: MsiIsProductElevated, MsiIsProductElevated function, MsiIsProductElevatedA, MsiIsProductElevatedW, _msi_msiisproductelevated, msi/MsiIsProductElevated, msi/MsiIsProductElevatedA, msi/MsiIsProductElevatedW, setup.msiisproductelevated
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiIsProductElevatedW (Unicode) and MsiIsProductElevatedA (ANSI)
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
 - MsiIsProductElevatedA
 - msi/MsiIsProductElevatedA
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
 - MsiIsProductElevated
 - MsiIsProductElevatedA
 - MsiIsProductElevatedW
---

# MsiIsProductElevatedA function


## -description

The <b>MsiIsProductElevated</b> function returns whether or not the product is managed. Only applications that require elevated privileges for installation and being installed through advertisement are considered managed, which means that an application installed per-machine is always considered managed. 

An application that is installed  per-user is only considered managed if it is advertised by a local system process that is impersonating the user. For more information, see <a href="/windows/desktop/Msi/advertising-a-per-user-application-to-be-installed-with-elevated-privileges">Advertising a Per-User Application to be Installed with Elevated Privileges</a>.
     

<b>MsiIsProductElevated</b> verifies that the local system owns the product registry data. The function does not refer to account policies such as <a href="/windows/desktop/Msi/alwaysinstallelevated">AlwaysInstallElevated</a>.

## -parameters

### -param szProduct [in]

The full product code GUID of the product. 

This parameter is required and cannot be <b>NULL</b> or empty.

### -param pfElevated [out]

A pointer to a BOOL for the result. 

This parameter cannot be <b>NULL</b>.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS, and <i>pfElevated</i> is set to <b>TRUE</b> if the product is a managed application.

If the function fails, the return value is one of the error codes identified in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PRODUCT</b></dt>
</dl>
</td>
<td width="60%">
The product is not currently known.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument is passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_CONFIGURATION</b></dt>
</dl>
</td>
<td width="60%">
The configuration information for the product is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FUNCTION_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The function failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CALL_NOT_IMPLEMENTED</b></dt>
</dl>
</td>
<td width="60%">
The function is not available for a specific platform. 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Msi/determining-installation-context">Determining Installation Context</a>



<a href="/windows/desktop/Msi/installing-a-package-with-elevated-privileges-for-a-non-admin">Installing a Package with Elevated Privileges for a Non-Admin</a>

## -remarks

> [!NOTE]
> The msi.h header defines MsiIsProductElevated as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
