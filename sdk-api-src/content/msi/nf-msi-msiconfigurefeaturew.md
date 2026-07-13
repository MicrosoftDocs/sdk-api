---
UID: NF:msi.MsiConfigureFeatureW
title: MsiConfigureFeatureW function (msi.h)
description: The MsiConfigureFeature function configures the installed state for a product feature. (Unicode)
helpviewer_keywords: ["INSTALLSTATE_ABSENT", "INSTALLSTATE_ADVERTISED", "INSTALLSTATE_DEFAULT", "INSTALLSTATE_LOCAL", "INSTALLSTATE_SOURCE", "MsiConfigureFeature", "MsiConfigureFeature function", "MsiConfigureFeatureW", "_msi_msiconfigurefeature", "msi/MsiConfigureFeature", "msi/MsiConfigureFeatureW", "setup.msiconfigurefeature"]
old-location: setup\msiconfigurefeature.htm
tech.root: setup
ms.assetid: 067d6fbb-833f-4e0e-bfdb-18d1b8608f58
ms.date: 12/05/2018
ms.keywords: INSTALLSTATE_ABSENT, INSTALLSTATE_ADVERTISED, INSTALLSTATE_DEFAULT, INSTALLSTATE_LOCAL, INSTALLSTATE_SOURCE, MsiConfigureFeature, MsiConfigureFeature function, MsiConfigureFeatureA, MsiConfigureFeatureW, _msi_msiconfigurefeature, msi/MsiConfigureFeature, msi/MsiConfigureFeatureA, msi/MsiConfigureFeatureW, setup.msiconfigurefeature
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiConfigureFeatureW (Unicode) and MsiConfigureFeatureA (ANSI)
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
 - MsiConfigureFeatureW
 - msi/MsiConfigureFeatureW
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
 - MsiConfigureFeature
 - MsiConfigureFeatureA
 - MsiConfigureFeatureW
---

# MsiConfigureFeatureW function


## -description

The 
<b>MsiConfigureFeature</b> function configures the installed state for a product feature.

## -parameters

### -param szProduct [in]

Specifies the product code for the product to be configured.

### -param szFeature [in]

Specifies the feature ID for the feature to be configured.

### -param eInstallState [in]

Specifies the installation state for the feature. This parameter must be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_ADVERTISED"></a><a id="installstate_advertised"></a><dl>
<dt><b>INSTALLSTATE_ADVERTISED</b></dt>
</dl>
</td>
<td width="60%">
The feature is advertised

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_LOCAL"></a><a id="installstate_local"></a><dl>
<dt><b>INSTALLSTATE_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
The feature is installed locally.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_ABSENT"></a><a id="installstate_absent"></a><dl>
<dt><b>INSTALLSTATE_ABSENT</b></dt>
</dl>
</td>
<td width="60%">
The feature is uninstalled.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_SOURCE"></a><a id="installstate_source"></a><dl>
<dt><b>INSTALLSTATE_SOURCE</b></dt>
</dl>
</td>
<td width="60%">
The feature is installed to run from source.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_DEFAULT"></a><a id="installstate_default"></a><dl>
<dt><b>INSTALLSTATE_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The feature is installed to its default location.

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
The function succeeds.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>An error relating to an action</b></dt>
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
An error that relates to the initialization has occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Msi/displayed-error-messages">Displayed Error Messages</a>



<a href="/windows/desktop/Msi/error-codes">Error Codes</a>



<a href="/windows/desktop/Msi/initialization-errors">Initialization Error</a>



<a href="/windows/desktop/Msi/installer-function-reference">Installation and Configuration Functions</a>



<a href="/windows/desktop/Msi/multiple-package-installations">Multiple-Package Installations</a>

## -remarks

> [!NOTE]
> The msi.h header defines MsiConfigureFeature as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
