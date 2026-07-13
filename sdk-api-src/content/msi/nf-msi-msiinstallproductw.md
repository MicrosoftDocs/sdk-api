---
UID: NF:msi.MsiInstallProductW
title: MsiInstallProductW function (msi.h)
description: Installs or uninstalls a product. (MsiInstallProductW)
helpviewer_keywords: ["MsiInstallProduct", "MsiInstallProduct function", "MsiInstallProductW", "_msi_msiinstallproduct", "msi/MsiInstallProduct", "msi/MsiInstallProductW", "setup.msiinstallproduct"]
old-location: setup\msiinstallproduct.htm
tech.root: setup
ms.assetid: ec8d6710-ecfe-432c-ba1d-2e3532a25988
ms.date: 12/05/2018
ms.keywords: MsiInstallProduct, MsiInstallProduct function, MsiInstallProductA, MsiInstallProductW, _msi_msiinstallproduct, msi/MsiInstallProduct, msi/MsiInstallProductA, msi/MsiInstallProductW, setup.msiinstallproduct
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiInstallProductW (Unicode) and MsiInstallProductA (ANSI)
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
 - MsiInstallProductW
 - msi/MsiInstallProductW
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
 - MsiInstallProduct
 - MsiInstallProductA
 - MsiInstallProductW
---

# MsiInstallProductW function


## -description

The 
<b>MsiInstallProduct</b> function installs or uninstalls a product.

## -parameters

### -param szPackagePath [in]

A null-terminated string that specifies the path to the location of the Windows Installer package. The string value can contain a URL (e.g. <code>http://packageLocation/package/package.msi</code>), a network path  (e.g. \\packageLocation\package.msi), a file path (e.g. file://packageLocation/package.msi), or a local path (e.g. D:\packageLocation\package.msi).

### -param szCommandLine [in]

A null-terminated string that specifies the command line property settings. This should be a list of the format <i>Property=Setting Property=Setting</i>. For more information, see 
<a href="/windows/desktop/Msi/about-properties">About Properties</a>.

To perform an administrative installation, include ACTION=ADMIN in <i>szCommandLine</i>. For more information, see the 
<a href="/windows/desktop/Msi/action">ACTION</a> property.

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function completes successfully.

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
An error that relates to initialization occurred.

</td>
</tr>
</table>
 

For more information, see 
<a href="/windows/desktop/Msi/displayed-error-messages">Displayed Error Messages</a>.

## -remarks

The 
<b>MsiInstallProduct</b> function displays the user interface with the current settings and log mode.

<ul>
<li>You can change user interface settings by using the 
<a href="/windows/desktop/api/msi/nf-msi-msisetinternalui">MsiSetInternalUI</a>, 
<a href="/windows/desktop/api/msi/nf-msi-msisetexternaluia">MsiSetExternalUI</a>, or <a href="/windows/desktop/api/msi/nf-msi-msisetexternaluirecord">MsiSetExternalUIRecord</a> functions.</li>
<li>You can set the log mode by using the 
<a href="/windows/desktop/api/msi/nf-msi-msienableloga">MsiEnableLog</a> function.</li>
<li>You can completely remove a product by setting REMOVE=ALL in <i>szCommandLine</i>.</li>
</ul>
For more information, see 
<a href="/windows/desktop/Msi/remove">REMOVE</a> Property.





> [!NOTE]
> The msi.h header defines MsiInstallProduct as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/displayed-error-messages">Displayed Error Messages</a>



<a href="/windows/desktop/Msi/error-codes">Error Codes</a>



<a href="/windows/desktop/Msi/initialization-errors">Initialization Error</a>



<a href="/windows/desktop/Msi/installer-function-reference">Installation and Configuration Functions</a>



<a href="/windows/desktop/Msi/multiple-package-installations">Multiple-Package Installations</a>
