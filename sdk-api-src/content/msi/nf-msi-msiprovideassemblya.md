---
UID: NF:msi.MsiProvideAssemblyA
title: MsiProvideAssemblyA function (msi.h)
description: The MsiProvideAssembly function returns the full path to a Windows Installer component that contains an assembly. The function prompts for a source and performs any necessary installation. MsiProvideAssembly increments the usage count for the feature. (ANSI)
helpviewer_keywords: ["INSTALLMODE_DEFAULT", "INSTALLMODE_EXISTING", "INSTALLMODE_NODETECTION", "INSTALLMODE_NODETECTION_ANY", "INSTALLMODE_NOSOURCERESOLUTION", "MSIASSEMBLYINFO_NETASSEMBLY", "MSIASSEMBLYINFO_WIN32ASSEMBLY", "MsiProvideAssemblyA", "combination of the REINSTALLMODE flags", "msi/MsiProvideAssemblyA"]
old-location: setup\msiprovideassembly.htm
tech.root: setup
ms.assetid: 9d7deb0b-f247-4af0-ba94-4d40c2f31109
ms.date: 12/05/2018
ms.keywords: INSTALLMODE_DEFAULT, INSTALLMODE_EXISTING, INSTALLMODE_NODETECTION, INSTALLMODE_NODETECTION_ANY, INSTALLMODE_NOSOURCERESOLUTION, MSIASSEMBLYINFO_NETASSEMBLY, MSIASSEMBLYINFO_WIN32ASSEMBLY, MsiProvideAssembly, MsiProvideAssembly function, MsiProvideAssemblyA, MsiProvideAssemblyW, _msi_msiprovideassembly, combination of the REINSTALLMODE flags, msi/MsiProvideAssembly, msi/MsiProvideAssemblyA, msi/MsiProvideAssemblyW, setup.msiprovideassembly
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiProvideAssemblyW (Unicode) and MsiProvideAssemblyA (ANSI)
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
 - MsiProvideAssemblyA
 - msi/MsiProvideAssemblyA
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
 - MsiProvideAssembly
 - MsiProvideAssemblyA
 - MsiProvideAssemblyW
---

# MsiProvideAssemblyA function


## -description

The 
<b>MsiProvideAssembly</b> function returns the full path to a Windows Installer component that contains an assembly. The function prompts for a source and performs any necessary installation. 
<b>MsiProvideAssembly</b> increments the usage count for the feature.

## -parameters

### -param szAssemblyName [in]

The assembly name as a string.

### -param szAppContext [in]

Set to null for global assemblies. For private assemblies, set <i>szAppContext</i> to the full path of the application configuration file  or to the full path of the executable file of the application to which the assembly has been made private.

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
<td width="40%"><a id="INSTALLMODE_NOSOURCERESOLUTION"></a><a id="installmode_nosourceresolution"></a><dl>
<dt><b>INSTALLMODE_NOSOURCERESOLUTION</b></dt>
</dl>
</td>
<td width="60%">
Provide the component only if the feature's installation state is INSTALLSTATE_LOCAL. If the feature installation state is INSTALLSTATE_SOURCE, return ERROR_INSTALL_SOURCE_ABSENT. Otherwise return ERROR_FILE_NOT_FOUND. This mode only checks that the component is registered and does not verify that the key file exists.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLMODE_NODETECTION_ANY"></a><a id="installmode_nodetection_any"></a><dl>
<dt><b>INSTALLMODE_NODETECTION_ANY</b></dt>
</dl>
</td>
<td width="60%">
Provide the component if a feature exists from any installed product. Otherwise return ERROR_FILE_NOT_FOUND. This mode only checks that the component is registered and does not verify that the key file of the component exists. 
This flag is similar to the INSTALLMODE_NODETECTION flag except that with this flag we check for any product that has installed the assembly as opposed to the last product as is the case with the INSTALLMODE_NODETECTION flag.
This flag can only be used with <b>MsiProvideAssembly</b>.

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
</table>

### -param dwAssemblyInfo [in]

Assembly information and assembly type. Set to one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSIASSEMBLYINFO_NETASSEMBLY"></a><a id="msiassemblyinfo_netassembly"></a><dl>
<dt><b>MSIASSEMBLYINFO_NETASSEMBLY</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
.NET Assembly

</td>
</tr>
<tr>
<td width="40%"><a id="MSIASSEMBLYINFO_WIN32ASSEMBLY"></a><a id="msiassemblyinfo_win32assembly"></a><dl>
<dt><b>MSIASSEMBLYINFO_WIN32ASSEMBLY</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Win32 Assembly

</td>
</tr>
</table>

### -param lpPathBuf [out]

Pointer to a variable that receives the path to the component. This parameter can be null.

### -param pcchPathBuf [in, out]

Pointer to a variable that specifies the size, in characters, of the buffer pointed to by the <i>lpPathBuf</i> parameter. On input, this is the full size of the buffer, including a space for a terminating null character. If the buffer passed in is too small, the count returned does not include the terminating null character. 




If <i>lpPathBuf</i> is null, <i>pcchPathBuf</i> can be null.

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
The feature is absent or broken. This error is returned for dwInstallMode = INSTALLMODE_EXISTING.

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
<dt><b>ERROR_UNKNOWN_COMPONENT</b></dt>
</dl>
</td>
<td width="60%">
The component ID does not specify a known component.

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
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system does not have enough memory to complete the operation. Available with Windows Server 2003.

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

When the 
<b>MsiProvideAssembly</b> function succeeds, the <i>pcchPathBuf</i> parameter contains the length of the string in <i>lpPathBuf</i>.

The INSTALLMODE_EXISTING option cannot be used in combination with the REINSTALLMODE flag.

Features with components that contain a corrupted file or the wrong version of a file must be explicitly reinstalled by the user, or by having the application call 
<a href="/windows/desktop/api/msi/nf-msi-msireinstallfeaturea">MsiReinstallFeature</a>.





> [!NOTE]
> The msi.h header defines MsiProvideAssembly as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">Component-Specific Functions</a>



<a href="/windows/desktop/Msi/multiple-package-installations">Multiple-Package Installations</a>
