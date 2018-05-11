---
UID: NF:msi.MsiProvideAssemblyW
title: MsiProvideAssemblyW function
author: windows-driver-content
description: The MsiProvideAssembly function returns the full path to a Windows Installer component that contains an assembly. The function prompts for a source and performs any necessary installation. MsiProvideAssembly increments the usage count for the feature.
old-location: setup\msiprovideassembly.htm
old-project: Msi
ms.assetid: 9d7deb0b-f247-4af0-ba94-4d40c2f31109
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: INSTALLMODE_DEFAULT, INSTALLMODE_EXISTING, INSTALLMODE_NODETECTION, INSTALLMODE_NODETECTION_ANY, INSTALLMODE_NOSOURCERESOLUTION, MSIASSEMBLYINFO_NETASSEMBLY, MSIASSEMBLYINFO_WIN32ASSEMBLY, MsiProvideAssembly, MsiProvideAssembly function, MsiProvideAssemblyA, MsiProvideAssemblyW, _msi_msiprovideassembly, combination of the REINSTALLMODE flags, msi/MsiProvideAssembly, msi/MsiProvideAssemblyA, msi/MsiProvideAssemblyW, setup.msiprovideassembly
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: DRM_CLIENT_VERSION_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msi.dll
api_name:
-	MsiProvideAssembly
-	MsiProvideAssemblyA
-	MsiProvideAssemblyW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# MsiProvideAssemblyW function


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
<a href="https://msdn.microsoft.com/0750838d-56c8-449c-b1fd-99c9426beb52">MsiReinstallFeature</a> with the following flag bits set: REINSTALLMODE_FILEMISSING, REINSTALLMODE_FILEOLDERVERSION, REINSTALLMODE_FILEVERIFY, REINSTALLMODE_MACHINEDATA, REINSTALLMODE_USERDATA and REINSTALLMODE_SHORTCUT.

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
<a href="https://msdn.microsoft.com/0750838d-56c8-449c-b1fd-99c9426beb52">MsiReinstallFeature</a> to reinstall feature using this parameter for the <i>dwReinstallMode</i> parameter, and then provide the component.

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
<a href="https://msdn.microsoft.com/0153a21f-9b26-4088-b12b-96c9e6918cc3">Displayed Error Messages</a>.




## -remarks



When the 
<b>MsiProvideAssembly</b> function succeeds, the <i>pcchPathBuf</i> parameter contains the length of the string in <i>lpPathBuf</i>.

The INSTALLMODE_EXISTING option cannot be used in combination with the REINSTALLMODE flag.

Features with components that contain a corrupted file or the wrong version of a file must be explicitly reinstalled by the user, or by having the application call 
<a href="https://msdn.microsoft.com/0750838d-56c8-449c-b1fd-99c9426beb52">MsiReinstallFeature</a>.




## -see-also




<a href="https://msdn.microsoft.com/05a16915-6b47-4d51-b62a-5a4d92b87e50">Component-Specific Functions</a>



<a href="https://msdn.microsoft.com/c4a0f4d8-818d-4e60-908b-adaa2a54de95">Multiple-Package Installations</a>
 

 

