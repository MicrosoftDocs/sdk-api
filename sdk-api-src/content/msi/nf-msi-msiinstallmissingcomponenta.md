---
UID: NF:msi.MsiInstallMissingComponentA
title: MsiInstallMissingComponentA function (msi.h)
description: The MsiInstallMissingComponent function installs files that are unexpectedly missing. (ANSI)
helpviewer_keywords: ["INSTALLSTATE_DEFAULT", "INSTALLSTATE_LOCAL", "INSTALLSTATE_SOURCE", "MsiInstallMissingComponentA", "msi/MsiInstallMissingComponentA"]
old-location: setup\msiinstallmissingcomponent.htm
tech.root: setup
ms.assetid: 81b44b77-e972-409c-b933-8fcae8887266
ms.date: 12/05/2018
ms.keywords: INSTALLSTATE_DEFAULT, INSTALLSTATE_LOCAL, INSTALLSTATE_SOURCE, MsiInstallMissingComponent, MsiInstallMissingComponent function, MsiInstallMissingComponentA, MsiInstallMissingComponentW, _msi_msiinstallmissingcomponent, msi/MsiInstallMissingComponent, msi/MsiInstallMissingComponentA, msi/MsiInstallMissingComponentW, setup.msiinstallmissingcomponent
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiInstallMissingComponentW (Unicode) and MsiInstallMissingComponentA (ANSI)
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
 - MsiInstallMissingComponentA
 - msi/MsiInstallMissingComponentA
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
 - MsiInstallMissingComponent
 - MsiInstallMissingComponentA
 - MsiInstallMissingComponentW
---

# MsiInstallMissingComponentA function


## -description

The 
<b>MsiInstallMissingComponent</b> function installs files that are unexpectedly missing.

## -parameters

### -param szProduct [in]

Specifies the product code for the product that owns the component to be installed.

### -param szComponent [in]

Identifies the component to be installed.

### -param eInstallState [in]

Specifies the way the component should be installed. This parameter must be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_LOCAL"></a><a id="installstate_local"></a><dl>
<dt><b>INSTALLSTATE_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
The component should be locally installed.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_SOURCE"></a><a id="installstate_source"></a><dl>
<dt><b>INSTALLSTATE_SOURCE</b></dt>
</dl>
</td>
<td width="60%">
The component should be installed to run from the source.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_DEFAULT"></a><a id="installstate_default"></a><dl>
<dt><b>INSTALLSTATE_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The component should be installed according to the installer defaults.

</td>
</tr>
</table>

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_CONFIGURATION</b></dt>
</dl>
</td>
<td width="60%">
The configuration information is corrupt.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The installation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_SOURCE_ABSENT</b></dt>
</dl>
</td>
<td width="60%">
The source was unavailable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_SUSPEND</b></dt>
</dl>
</td>
<td width="60%">
The installation was suspended.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_USEREXIT</b></dt>
</dl>
</td>
<td width="60%">
The user exited the installation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PRODUCT</b></dt>
</dl>
</td>
<td width="60%">
The product code is unrecognized.

</td>
</tr>
</table>
 

For more information about error messages, see 
<a href="/windows/desktop/Msi/displayed-error-messages">Displayed Error Messages</a>

## -remarks

The 
<b>MsiInstallMissingComponent</b> function resolves the feature(s) that the component belongs to. Then, the product feature that requires the least additional disk space is installed.





> [!NOTE]
> The msi.h header defines MsiInstallMissingComponent as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/multiple-package-installations">Multiple-Package Installations</a>
