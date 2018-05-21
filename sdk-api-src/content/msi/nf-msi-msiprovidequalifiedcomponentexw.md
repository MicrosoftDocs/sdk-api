---
UID: NF:msi.MsiProvideQualifiedComponentExW
title: MsiProvideQualifiedComponentExW function
author: windows-driver-content
description: The MsiProvideQualifiedComponentEx function returns the full component path for a qualified component that is published by a product and performs any necessary installation.
old-location: setup\msiprovidequalifiedcomponentex.htm
old-project: Msi
ms.assetid: b8b567de-c21a-4e8f-840c-e71f41c11447
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: INSTALLMODE_DEFAULT, INSTALLMODE_EXISTING, INSTALLMODE_NODETECTION, INSTALLMODE_NOSOURCERESOLUTION, MsiProvideQualifiedComponentEx, MsiProvideQualifiedComponentEx function, MsiProvideQualifiedComponentExA, MsiProvideQualifiedComponentExW, _msi_msiprovidequalifiedcomponentex, combination of the REINSTALLMODE flags, msi/MsiProvideQualifiedComponentEx, msi/MsiProvideQualifiedComponentExA, msi/MsiProvideQualifiedComponentExW, setup.msiprovidequalifiedcomponentex
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
req.unicode-ansi: MsiProvideQualifiedComponentExW (Unicode) and MsiProvideQualifiedComponentExA (ANSI)
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
-	MsiProvideQualifiedComponentEx
-	MsiProvideQualifiedComponentExA
-	MsiProvideQualifiedComponentExW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# MsiProvideQualifiedComponentExW function


## -description


The 
<b>MsiProvideQualifiedComponentEx</b> function returns the full component path for a qualified component that is published by a product and performs any necessary installation. This function prompts for source if necessary and increments the usage count for the feature.


## -parameters




### -param szCategory

TBD


### -param szQualifier [in]

Specifies a qualifier into a list of advertising components (from 
<a href="https://msdn.microsoft.com/4a6be647-3e73-47a1-acfa-7d6d0a2fb2f4">PublishComponent Table</a>).


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
<td width="40%"><a id="INSTALLMODE_EXISTING"></a><a id="installmode_existing"></a><dl>
<dt><b>INSTALLMODE_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
Provide the component only if the feature exists, else return ERROR_FILE_NOT_FOUND.

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
 


### -param szProduct [in]

Specifies the product to match that has published the qualified component. If this is null, then this API works the same as 
<a href="https://msdn.microsoft.com/1d37e2c4-3ee0-42d2-95de-6e058319a4d4">MsiProvideQualifiedComponent</a>.


### -param dwUnused1 [in]

Reserved. Must be zero.


### -param dwUnused2 [in]

Reserved. Must be zero.


### -param lpPathBuf [out]

Pointer to a variable that receives the path to the component. This parameter can be null.


### -param pcchPathBuf [in, out]

Pointer to a variable that specifies the size, in characters, of the buffer pointed to by the <i>lpPathBuf</i> parameter. On input, this is the full size of the buffer, including a space for a terminating null character. If the buffer passed in is too small, the count returned does not include the terminating null character. 




If <i>lpPathBuf</i> is null, <i>pcchBuf</i> can be null.


#### - szComponent [in]

Specifies the component ID that for the requested component. This may not be the GUID for the component itself but rather a server that provides the correct functionality, as in the ComponentId column of the 
<a href="https://msdn.microsoft.com/4a6be647-3e73-47a1-acfa-7d6d0a2fb2f4">PublishComponent table</a>.


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
Component qualifier invalid or not present.

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
The feature is absent or broken. this error is returned for <i>dwInstallMode</i> = INSTALLMODE_EXISTING.

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
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/5cce27ff-1143-4fe6-b4bd-727581431c07">Initialization Error</a></b></dt>
</dl>
</td>
<td width="60%">
An error relating to initialization occurred.

</td>
</tr>
</table>
 




## -remarks



Upon success of the 
<b>MsiProvideQualifiedComponentEx</b> function, the <i>pcchPathBuf</i> parameter contains the length of the string in <i>lpPathBuf</i>.

Features with components containing a corrupted file or the wrong version of a file must be explicitly reinstalled by the user or by having the application call 
<a href="https://msdn.microsoft.com/0750838d-56c8-449c-b1fd-99c9426beb52">MsiReinstallFeature</a>.




## -see-also




<a href="https://msdn.microsoft.com/05a16915-6b47-4d51-b62a-5a4d92b87e50">Component-Specific Functions</a>



<a href="https://msdn.microsoft.com/0153a21f-9b26-4088-b12b-96c9e6918cc3">Displayed Error Messages</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>



<a href="https://msdn.microsoft.com/5cce27ff-1143-4fe6-b4bd-727581431c07">Initialization Error</a>



<a href="https://msdn.microsoft.com/c4a0f4d8-818d-4e60-908b-adaa2a54de95">Multiple-Package Installations</a>
 

 

