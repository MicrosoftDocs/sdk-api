---
UID: NF:msi.MsiProvideQualifiedComponentW
title: MsiProvideQualifiedComponentW function (msi.h)
description: The MsiProvideQualifiedComponent function returns the full component path for a qualified component and performs any necessary installation. This function prompts for source if necessary, and increments the usage count for the feature. (Unicode)
helpviewer_keywords: ["INSTALLMODE_DEFAULT", "INSTALLMODE_EXISTING", "INSTALLMODE_NODETECTION", "INSTALLMODE_NOSOURCERESOLUTION", "MsiProvideQualifiedComponent", "MsiProvideQualifiedComponent function", "MsiProvideQualifiedComponentW", "_msi_msiprovidequalifiedcomponent", "combination of the REINSTALLMODE flags", "msi/MsiProvideQualifiedComponent", "msi/MsiProvideQualifiedComponentW", "setup.msiprovidequalifiedcomponent"]
old-location: setup\msiprovidequalifiedcomponent.htm
tech.root: setup
ms.assetid: 1d37e2c4-3ee0-42d2-95de-6e058319a4d4
ms.date: 12/05/2018
ms.keywords: INSTALLMODE_DEFAULT, INSTALLMODE_EXISTING, INSTALLMODE_NODETECTION, INSTALLMODE_NOSOURCERESOLUTION, MsiProvideQualifiedComponent, MsiProvideQualifiedComponent function, MsiProvideQualifiedComponentA, MsiProvideQualifiedComponentW, _msi_msiprovidequalifiedcomponent, combination of the REINSTALLMODE flags, msi/MsiProvideQualifiedComponent, msi/MsiProvideQualifiedComponentA, msi/MsiProvideQualifiedComponentW, setup.msiprovidequalifiedcomponent
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiProvideQualifiedComponentW (Unicode) and MsiProvideQualifiedComponentA (ANSI)
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
 - MsiProvideQualifiedComponentW
 - msi/MsiProvideQualifiedComponentW
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
 - MsiProvideQualifiedComponent
 - MsiProvideQualifiedComponentA
 - MsiProvideQualifiedComponentW
---

# MsiProvideQualifiedComponentW function


## -description

The 
<b>MsiProvideQualifiedComponent</b> function returns the full component path for a qualified component and performs any necessary installation. This function prompts for source if necessary, and increments the usage count for the feature.

## -parameters

### -param szCategory [in]

Specifies the component ID  for the requested component. This may not be the GUID for the component itself, but rather a server that provides the correct functionality, as in the ComponentId column of the 
<a href="/windows/desktop/Msi/publishcomponent-table">PublishComponent table</a>.

### -param szQualifier [in]

Specifies a qualifier into a list of advertising components (from 
<a href="/windows/desktop/Msi/publishcomponent-table">PublishComponent Table</a>).

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
<a href="/windows/desktop/api/msi/nf-msi-msireinstallfeaturea">MsiReinstallFeature</a> with the following flag bits set: REINSTALLMODE_FILEMISSING, REINSTALLMODE_FILEOLDERVERSION, REINSTALLMODE_FILEVERIFY, REINSTALLMODE_MACHINEDATA, REINSTALLMODE_USERDATA, and REINSTALLMODE_SHORTCUT.

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
<a href="/windows/desktop/api/msi/nf-msi-msireinstallfeaturea">MsiReinstallFeature</a> to reinstall the feature using this parameter for the <i>dwReinstallMode</i> parameter, and then provide the component.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMODE_NOSOURCERESOLUTION"></a><a id="installmode_nosourceresolution"></a><dl>
<dt><b>INSTALLMODE_NOSOURCERESOLUTION</b></dt>
</dl>
</td>
<td width="60%">
Provide the component only if the feature's installation state is INSTALLSTATE_LOCAL. If the feature's installation state is INSTALLSTATE_SOURCE, return ERROR_INSTALL_SOURCE_ABSENT. Otherwise, it returns ERROR_FILE_NOT_FOUND. This mode only checks that the component is registered and does not verify that the key file exists.

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
<dt><b>ERROR_INDEX_ABSENT</b></dt>
</dl>
</td>
<td width="60%">
The component qualifier is invalid or absent.

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
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The feature is absent or broken. This error is returned for dwInstallMode = INSTALLMODE_EXISTING.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_COMPONENT</b></dt>
</dl>
</td>
<td width="60%">
The specified component is unknown.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>An error relating to an action</b></dt>
</dl>
</td>
<td width="60%">
See 
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

Upon success of the 
<b>MsiProvideQualifiedComponent</b> function, the <i>pcchPathBuf</i> parameter contains the length of the string in <i>lpPathBuf</i>.

Features with components containing a corrupted file or the wrong version of a file must be explicitly reinstalled by the user or by having the application call 
<a href="/windows/desktop/api/msi/nf-msi-msireinstallfeaturea">MsiReinstallFeature</a>.





> [!NOTE]
> The msi.h header defines MsiProvideQualifiedComponent as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">Component-Specific Functions</a>



<a href="/windows/desktop/Msi/displayed-error-messages">Displayed Error Messages</a>



<a href="/windows/desktop/Msi/error-codes">Error Codes</a>



<a href="/windows/desktop/Msi/initialization-errors">Initialization Error</a>



<a href="/windows/desktop/Msi/multiple-package-installations">Multiple-Package Installations</a>
