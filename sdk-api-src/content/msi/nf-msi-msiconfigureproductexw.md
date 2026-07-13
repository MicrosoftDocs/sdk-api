---
UID: NF:msi.MsiConfigureProductExW
title: MsiConfigureProductExW function (msi.h)
description: Installs or uninstalls a product. (MsiConfigureProductExW)
helpviewer_keywords: ["INSTALLLEVEL_DEFAULT", "INSTALLLEVEL_MAXIMUM", "INSTALLLEVEL_MINIMUM", "INSTALLSTATE_ABSENT", "INSTALLSTATE_ADVERTISED", "INSTALLSTATE_DEFAULT", "INSTALLSTATE_LOCAL", "INSTALLSTATE_SOURCE", "MsiConfigureProductEx", "MsiConfigureProductEx function", "MsiConfigureProductExW", "_msi_msiconfigureproductex", "msi/MsiConfigureProductEx", "msi/MsiConfigureProductExW", "setup.msiconfigureproductex"]
old-location: setup\msiconfigureproductex.htm
tech.root: setup
ms.assetid: 7a7ae88a-b893-4d10-8542-b2066d1572a9
ms.date: 12/05/2018
ms.keywords: INSTALLLEVEL_DEFAULT, INSTALLLEVEL_MAXIMUM, INSTALLLEVEL_MINIMUM, INSTALLSTATE_ABSENT, INSTALLSTATE_ADVERTISED, INSTALLSTATE_DEFAULT, INSTALLSTATE_LOCAL, INSTALLSTATE_SOURCE, MsiConfigureProductEx, MsiConfigureProductEx function, MsiConfigureProductExA, MsiConfigureProductExW, _msi_msiconfigureproductex, msi/MsiConfigureProductEx, msi/MsiConfigureProductExA, msi/MsiConfigureProductExW, setup.msiconfigureproductex
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiConfigureProductExW (Unicode) and MsiConfigureProductExA (ANSI)
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
 - MsiConfigureProductExW
 - msi/MsiConfigureProductExW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
 - Ext-MS-Win-MSi-Misc-L1-1-0.dll
api_name:
 - MsiConfigureProductEx
 - MsiConfigureProductExA
 - MsiConfigureProductExW
---

# MsiConfigureProductExW function


## -description

The 
<b>MsiConfigureProductEx</b> function installs or uninstalls a product. A product command line can also be specified.

## -parameters

### -param szProduct [in]

Specifies the product code for the product to be configured.

### -param iInstallLevel [in]

Specifies how much of the product should be installed when installing the product to its default state. The <i>iInstallLevel</i> parameters are ignored, and all features are installed, if the <i>eInstallState</i> parameter is set to any value other than <b>INSTALLSTATE_DEFAULT</b>.

This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLLEVEL_DEFAULT"></a><a id="installlevel_default"></a><dl>
<dt><b>INSTALLLEVEL_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The authored default features are installed.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLEVEL_MINIMUM"></a><a id="installlevel_minimum"></a><dl>
<dt><b>INSTALLLEVEL_MINIMUM</b></dt>
</dl>
</td>
<td width="60%">
Only the required features are installed. You can specify a value between <b>INSTALLLEVEL_MINIMUM</b> and <b>INSTALLLEVEL_MAXIMUM</b> to install a subset of available features.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLEVEL_MAXIMUM"></a><a id="installlevel_maximum"></a><dl>
<dt><b>INSTALLLEVEL_MAXIMUM</b></dt>
</dl>
</td>
<td width="60%">
All features are installed. You can specify a value between <b>INSTALLLEVEL_MINIMUM</b> and <b>INSTALLLEVEL_MAXIMUM</b> to install a subset of available features.

</td>
</tr>
</table>

### -param eInstallState [in]

Specifies the installation state for the product. This parameter can be one of the following values.

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
The product is to be installed with all features installed locally.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_ABSENT"></a><a id="installstate_absent"></a><dl>
<dt><b>INSTALLSTATE_ABSENT</b></dt>
</dl>
</td>
<td width="60%">
The product is uninstalled.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_SOURCE"></a><a id="installstate_source"></a><dl>
<dt><b>INSTALLSTATE_SOURCE</b></dt>
</dl>
</td>
<td width="60%">
The product is to be installed with all features installed to run from source.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_DEFAULT"></a><a id="installstate_default"></a><dl>
<dt><b>INSTALLSTATE_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The product is to be installed with all features installed to the default states specified in the <a href="/windows/desktop/Msi/feature-table">Feature Table</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_ADVERTISED"></a><a id="installstate_advertised"></a><dl>
<dt><b>INSTALLSTATE_ADVERTISED</b></dt>
</dl>
</td>
<td width="60%">
The product is advertised.

</td>
</tr>
</table>

### -param szCommandLine [in]

Specifies the command-line property settings. This should be a list of the format <i>Property=Setting Property=Setting</i>. For more information, see 
<a href="/windows/desktop/Msi/about-properties">About Properties</a>.

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
An invalid parameter is passed to the function.

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
<dt><b>An error that relates to an action</b></dt>
</dl>
</td>
<td width="60%">
For more information, see 
<a href="/windows/desktop/Msi/error-codes">Error Codes</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/Msi/initialization-errors">Initialization Error</a></b></dt>
</dl>
</td>
<td width="60%">
An error relating to initialization occurred.

</td>
</tr>
</table>

## -remarks

The command line passed in as <i>szCommandLine</i> can contain any of the 
<a href="/windows/desktop/Msi/property-reference">Feature Installation Options Properties</a>. In this case, the <i>eInstallState</i> passed must be <b>INSTALLSTATE_DEFAULT</b>.

The <i>iInstallLevel</i> parameter is ignored and all features of the product are installed if the <i>eInstallState</i> parameter is set to any other value than <b>INSTALLSTATE_DEFAULT</b>. To control the installation of individual features when the <i>eInstallState</i> parameter is not set to <b>INSTALLSTATE_DEFAULT</b> use 
<a href="/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea">MsiConfigureFeature</a>.

The 
<b>MsiConfigureProductEx</b> function displays the user interface using the current settings. User interface settings can be changed with 
<a href="/windows/desktop/api/msi/nf-msi-msisetinternalui">MsiSetInternalUI</a>, <a href="/windows/desktop/api/msi/nf-msi-msisetexternaluia">MsiSetExternalUI</a>, or <a href="/windows/desktop/api/msi/nf-msi-msisetexternaluirecord">MsiSetExternalUIRecord</a>.





> [!NOTE]
> The msi.h header defines MsiConfigureProductEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/displayed-error-messages">Displayed Error Messages</a>



<a href="/windows/desktop/Msi/error-codes">Error Codes</a>



<a href="/windows/desktop/Msi/initialization-errors">Initialization Error</a>



<a href="/windows/desktop/Msi/installer-function-reference">Installation and Configuration Functions</a>



<a href="/windows/desktop/Msi/multiple-package-installations">Multiple-Package Installations</a>
