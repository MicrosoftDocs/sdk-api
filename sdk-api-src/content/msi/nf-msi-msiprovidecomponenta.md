---
UID: NF:msi.MsiProvideComponentA
title: MsiProvideComponentA function (msi.h)
description: The MsiProvideComponent function returns the full component path, performing any necessary installation. This function prompts for source if necessary and increments the usage count for the feature. (ANSI)
helpviewer_keywords: ["INSTALLMODE_DEFAULT", "INSTALLMODE_EXISTING", "INSTALLMODE_NODETECTION", "INSTALLMODE_NOSOURCERESOLUTION", "MsiProvideComponentA", "combination of the REINSTALLMODE flags", "msi/MsiProvideComponentA"]
old-location: setup\msiprovidecomponent.htm
tech.root: setup
ms.assetid: da6fa117-9152-4289-aa92-79903b84bd3e
ms.date: 12/05/2018
ms.keywords: INSTALLMODE_DEFAULT, INSTALLMODE_EXISTING, INSTALLMODE_NODETECTION, INSTALLMODE_NOSOURCERESOLUTION, MsiProvideComponent, MsiProvideComponent function, MsiProvideComponentA, MsiProvideComponentW, _msi_msiprovidecomponent, combination of the REINSTALLMODE flags, msi/MsiProvideComponent, msi/MsiProvideComponentA, msi/MsiProvideComponentW, setup.msiprovidecomponent
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiProvideComponentW (Unicode) and MsiProvideComponentA (ANSI)
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
 - MsiProvideComponentA
 - msi/MsiProvideComponentA
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
 - MsiProvideComponent
 - MsiProvideComponentA
 - MsiProvideComponentW
---

# MsiProvideComponentA function


## -description

The 
<b>MsiProvideComponent</b> function returns the full component path, performing any necessary installation. This function prompts for source if necessary and increments the usage count for the feature.

## -parameters

### -param szProduct [in]

Specifies the product code for the product that contains the feature with the necessary component.

### -param szFeature [in]

Specifies the feature ID of the feature with the necessary component.

### -param szComponent [in]

Specifies the component code of the necessary component.

### -param dwInstallMode [in]

Defines the installation mode. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLMODE_DEFAULT"></a><a id="installmode_default"></a><dl>
<dt><b>INSTALLMODE_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Provide the component and perform any installation necessary to provide the component. If the key file of a component in the requested feature, or a feature parent, is missing, reinstall the feature using 
<a href="/windows/desktop/api/msi/nf-msi-msireinstallfeaturea">MsiReinstallFeature</a> with the following flag bits set: REINSTALLMODE_FILEMISSING, REINSTALLMODE_FILEOLDERVERSION, REINSTALLMODE_FILEVERIFY, REINSTALLMODE_MACHINEDATA, REINSTALLMODE_USERDATA and REINSTALLMODE_SHORTCUT.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMODE_EXISTING"></a><a id="installmode_existing"></a><dl>
<dt><b>INSTALLMODE_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
Provide the component only if the feature exists. Otherwise return ERROR_FILE_NOT_FOUND. 




This mode verifies that the key file of the component exists.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMODE_NODETECTION"></a><a id="installmode_nodetection"></a><dl>
<dt><b>INSTALLMODE_NODETECTION</b></dt>
</dl>
</td>
<td width="60%">
Provide the component only if the feature exists. Otherwise return ERROR_FILE_NOT_FOUND. 




This mode only checks that the component is registered and does not verify that the key file of the component exists.

</td>
</tr>
<tr>
<td width="40%"><a id="combination_of_the_REINSTALLMODE_flags"></a><a id="combination_of_the_reinstallmode_flags"></a><a id="COMBINATION_OF_THE_REINSTALLMODE_FLAGS"></a><dl>
<dt><b>combination of the
REINSTALLMODE flags</b></dt>
</dl>
</td>
<td width="60%">
Call 
<a href="/windows/desktop/api/msi/nf-msi-msireinstallfeaturea">MsiReinstallFeature</a> to reinstall feature using this parameter for the <i>dwReinstallMode</i> parameter, and then provide the component.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMODE_NOSOURCERESOLUTION"></a><a id="installmode_nosourceresolution"></a><dl>
<dt><b>INSTALLMODE_NOSOURCERESOLUTION</b></dt>
</dl>
</td>
<td width="60%">
Provide the component only if the feature's installation state is INSTALLSTATE_LOCAL. If the feature's installation state is INSTALLSTATE_SOURCE, return ERROR_INSTALL_SOURCE_ABSENT. Otherwise return ERROR_FILE_NOT_FOUND. This mode only checks that the component is registered and does not verify that the key file exists.

</td>
</tr>
</table>

### -param lpPathBuf [out]

Pointer to a variable that receives the path to the component. This parameter can be null.

### -param pcchPathBuf [in, out]

Pointer to a variable that specifies the size, in characters, of the buffer pointed to by the <i>lpPathBuf</i> parameter. On input, this is the full size of the buffer, including a space for a terminating null character. If the buffer passed in is too small, the count returned does not include the terminating null character. 




If <i>lpPathBuf</i> is null, <i>pcchBuf</i> can be null.

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
The configuration data is corrupt.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The feature is absent or broken. this error is returned for dwInstallMode = INSTALLMODE_EXISTING.

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
<dt><b>ERROR_INSTALL_NOTUSED</b></dt>
</dl>
</td>
<td width="60%">
The component being requested is disabled on the computer.

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
The function completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_FEATURE</b></dt>
</dl>
</td>
<td width="60%">
The feature ID does not identify a known feature.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PRODUCT</b></dt>
</dl>
</td>
<td width="60%">
The product code does not identify a known product.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
An unrecognized product or a feature name was passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer overflow is returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_SOURCE_ABSENT</b></dt>
</dl>
</td>
<td width="60%">
Unable to detect a source.

</td>
</tr>
</table>
 

For more information, see 
<a href="/windows/desktop/Msi/displayed-error-messages">Displayed Error Messages</a>.

## -remarks

Upon success of the 
<b>MsiProvideComponent</b> function, the <i>pcchPathBuf</i> parameter contains the length of the string in <i>lpPathBuf</i>.

The 
<b>MsiProvideComponent</b> function combines the functionality of 
<a href="/windows/desktop/api/msi/nf-msi-msiusefeaturea">MsiUseFeature</a>, 
<a href="/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea">MsiConfigureFeature</a>, and 
<a href="/windows/desktop/api/msi/nf-msi-msigetcomponentpatha">MsiGetComponentPath</a>. You can use the 
<b>MsiProvideComponent</b> function to simplify the calling sequence. However, because this function increments the usage count, use it with caution to prevent inaccurate usage counts. The 
<b>MsiProvideComponent</b> function also provides less flexibility than the series of individual calls.

If the application is recovering from an unexpected situation, the application has probably already called 
<a href="/windows/desktop/api/msi/nf-msi-msiusefeaturea">MsiUseFeature</a> and incremented the usage count. In this case, the application should call 
<a href="/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea">MsiConfigureFeature</a> instead of 
<b>MsiProvideComponent</b> to avoid incrementing the count again.

The INSTALLMODE_EXISTING option cannot be used in combination with the REINSTALLMODE flag.

Features with components containing a corrupted file or the wrong version of a file must be explicitly reinstalled by the user or by having the application call 
<a href="/windows/desktop/api/msi/nf-msi-msireinstallfeaturea">MsiReinstallFeature</a>.





> [!NOTE]
> The msi.h header defines MsiProvideComponent as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">Component-Specific Functions</a>



<a href="/windows/desktop/Msi/multiple-package-installations">Multiple-Package Installations</a>
