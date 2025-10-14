---
UID: NF:msi.MsiGetComponentPathExW
title: MsiGetComponentPathExW function (msi.h)
description: Returns the full path to an installed component. (Unicode)
helpviewer_keywords: ["HKEY_CLASSES_ROOT", "HKEY_CURRENT_USER", "HKEY_LOCAL_MACHINE", "HKEY_USERS", "MSIINSTALLCONTEXT_MACHINE", "MSIINSTALLCONTEXT_USERMANAGED", "MSIINSTALLCONTEXT_USERUNMANAGED", "MsiGetComponentPathEx", "MsiGetComponentPathEx function [Setup API]", "MsiGetComponentPathExW", "NULL", "User SID", "msi/MsiGetComponentPathEx", "msi/MsiGetComponentPathExW", "s-1-1-0", "setup.msigetcomponentpathex"]
old-location: setup\msigetcomponentpathex.htm
tech.root: setup
ms.assetid: 7501df09-170d-4f23-9404-d86e861ac7da
ms.date: 12/05/2018
ms.keywords: HKEY_CLASSES_ROOT, HKEY_CURRENT_USER, HKEY_LOCAL_MACHINE, HKEY_USERS, MSIINSTALLCONTEXT_MACHINE, MSIINSTALLCONTEXT_USERMANAGED, MSIINSTALLCONTEXT_USERUNMANAGED, MsiGetComponentPathEx, MsiGetComponentPathEx function [Setup API], MsiGetComponentPathExA, MsiGetComponentPathExW, NULL, User SID, msi/MsiGetComponentPathEx, msi/MsiGetComponentPathExA, msi/MsiGetComponentPathExW, s-1-1-0, setup.msigetcomponentpathex
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiGetComponentPathExW (Unicode) and MsiGetComponentPathExA (ANSI)
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
 - MsiGetComponentPathExW
 - msi/MsiGetComponentPathExW
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
 - MsiGetComponentPathEx
 - MsiGetComponentPathExA
 - MsiGetComponentPathExW
---

# MsiGetComponentPathExW function


## -description

The 
<b>MsiGetComponentPathEx</b> function returns the full path to an installed component. If the key path for the component is a registry key then the function returns the registry key.

This function extends the existing <a href="/windows/desktop/api/msi/nf-msi-msigetcomponentpatha">MsiGetComponentPath</a> function to enable searches for components across user accounts and installation contexts.

## -parameters

### -param szProductCode [in]

A null-terminated string value that specifies an application's product code GUID. The function gets  the path of installed components used by this application.

### -param szComponentCode [in]

A null-terminated string value that specifies a component code GUID. The function gets the path of an installed component having this component code.

### -param szUserSid [in, optional]

A  null-terminated string value that specifies the security identifier (SID) for a user in the system.  The function gets the paths of installed components  of applications installed under the user accounts identified by this SID. The special SID string s-1-1-0 (Everyone) specifies all users in the system. If this parameter is <b>NULL</b>, the function gets the path of an installed component for the currently logged-on user only.

<table>
<tr>
<th>SID type</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NULL"></a><a id="null"></a><dl>
<dt><b>NULL</b></dt>
</dl>
</td>
<td width="60%">
Specifies the currently logged-on user.

</td>
</tr>
<tr>
<td width="40%"><a id="User_SID"></a><a id="user_sid"></a><a id="USER_SID"></a><dl>
<dt><b>User SID</b></dt>
</dl>
</td>
<td width="60%">
Specifies a particular user in the system. An example of an user SID is "S-1-3-64-2415071341-1358098788-3127455600-2561".

</td>
</tr>
<tr>
<td width="40%"><a id="s-1-1-0"></a><a id="S-1-1-0"></a><dl>
<dt><b>s-1-1-0</b></dt>
</dl>
</td>
<td width="60%">
Specifies all users in the system.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  The special SID string s-1-5-18 (System) cannot be used to search applications installed in the per-machine installation context.  Setting the SID value to s-1-5-18 returns <b>ERROR_INVALID_PARAMETER</b>. When <i>dwContext</i> is set to MSIINSTALLCONTEXT_MACHINE only, <i>szUserSid</i> must be <b>NULL</b>.</div>
<div> </div>

### -param dwContext [in, optional]

A flag that specifies the installation context. The function gets the paths of installed components of applications installed in the specified installation context. This parameter can be a combination of the following values.

<table>
<tr>
<th>Context</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERMANAGED"></a><a id="msiinstallcontext_usermanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERMANAGED</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Include applications installed  in  the per–user–managed installation context. 

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERUNMANAGED"></a><a id="msiinstallcontext_userunmanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERUNMANAGED</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Include applications installed in  the per–user–unmanaged installation context.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_MACHINE"></a><a id="msiinstallcontext_machine"></a><dl>
<dt><b>MSIINSTALLCONTEXT_MACHINE</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Include applications installed in the per-machine installation context. When <i>dwInstallContext</i> is set to <b>MSIINSTALLCONTEXT_MACHINE</b> only, the <i>szUserSID</i> parameter must be <b>NULL</b>.


</td>
</tr>
</table>

### -param lpOutPathBuffer [out, optional]

A string value that receives the path to the component. This parameter can be <b>NULL</b>. If the component is a registry key, the registry roots are represented numerically. If this is a registry subkey path, there is a backslash at the end of the Key Path. If this is a registry value key path, there is no backslash at the end. For example, a registry path on a 32-bit operating system of <b>HKEY_CURRENT_USER</b>&#92;<b>SOFTWARE</b>&#92;<b>Microsoft</b> is returned as "01:\SOFTWARE\Microsoft\". The registry roots returned on 32-bit operating systems are defined as shown in the following table. 




<div class="alert"><b>Note</b>  On 64-bit operating systems, a value of 20 is added to the numerical registry roots in this table to distinguish them from registry key paths on 32-bit operating systems.
For example, a registry key path of <b>HKEY_CURRENT_USER</b>&#92;<b>SOFTWARE</b>&#92;<b>Microsoft</b> is returned as "21:\SOFTWARE\Microsoft\", if the component path is a registry key on a 64-bit operating system.</div>
<div> </div>


<table>
<tr>
<th>Root</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HKEY_CLASSES_ROOT"></a><a id="hkey_classes_root"></a><dl>
<dt><b>HKEY_CLASSES_ROOT</b></dt>
</dl>
</td>
<td width="60%">
00

</td>
</tr>
<tr>
<td width="40%"><a id="HKEY_CURRENT_USER"></a><a id="hkey_current_user"></a><dl>
<dt><b>HKEY_CURRENT_USER</b></dt>
</dl>
</td>
<td width="60%">
01

</td>
</tr>
<tr>
<td width="40%"><a id="HKEY_LOCAL_MACHINE"></a><a id="hkey_local_machine"></a><dl>
<dt><b>HKEY_LOCAL_MACHINE</b></dt>
</dl>
</td>
<td width="60%">
02

</td>
</tr>
<tr>
<td width="40%"><a id="HKEY_USERS"></a><a id="hkey_users"></a><dl>
<dt><b>HKEY_USERS</b></dt>
</dl>
</td>
<td width="60%">
03

</td>
</tr>
</table>

### -param pcchOutPathBuffer [in, out, optional]

Pointer to a location that receives the size of the buffer, in <b>TCHAR</b>, pointed to by the <i>szPathBuf</i> parameter.  The value in this location should be set to the count of  <b>TCHAR</b> in the string including the terminating null character. If the size of the  buffer  is too small, this parameter receives the length of the string value without including the terminating null character in the count.

## -returns

The 
<b>MsiGetComponentPathEx</b> function returns the following values.
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_NOTUSED</b></dt>
</dl>
</td>
<td width="60%">
The component being requested is disabled on the computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_BADCONFIG</b></dt>
</dl>
</td>
<td width="60%">
Configuration data is corrupt.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_ABSENT</b></dt>
</dl>
</td>
<td width="60%">
The component is not installed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the function parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
The component is installed locally.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_SOURCE</b></dt>
</dl>
</td>
<td width="60%">
The component is installed to run from source.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_SOURCEABSENT</b></dt>
</dl>
</td>
<td width="60%">
The component source is inaccessible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The product code or component ID is unknown.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_BROKEN</b></dt>
</dl>
</td>
<td width="60%">
The component is corrupt or partially missing in some way and requires repair.

</td>
</tr>
</table>

## -remarks

The 
<b>MsiGetComponentPathEx</b> function might return <b>INSTALLSTATE_ABSENT</b> or <b>INSTALL_STATE_UNKNOWN</b>, for the following reasons:

<ul>
<li>INSTALLSTATE_ABSENT 


The application did not properly ensure that the feature was installed by calling 
<a href="/windows/desktop/api/msi/nf-msi-msiusefeaturea">MsiUseFeature</a> and, if necessary, 
<a href="/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea">MsiConfigureFeature</a>.

</li>
<li>INSTALLSTATE_UNKNOWN 


The feature is not published. The application should have determined this earlier by calling 
<a href="/windows/desktop/api/msi/nf-msi-msiqueryfeaturestatea">MsiQueryFeatureState</a> or 
<a href="/windows/desktop/api/msi/nf-msi-msienumfeaturesa">MsiEnumFeatures</a>. The application makes these calls while it initializes. An application should only use features that are known to be published. Since INSTALLSTATE_UNKNOWN should have been returned by 
<a href="/windows/desktop/api/msi/nf-msi-msiusefeaturea">MsiUseFeature</a> as well, either 
<b>MsiUseFeature</b> was not called, or its return value was not properly checked.

</li>
</ul>




> [!NOTE]
> The msi.h header defines MsiGetComponentPathEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">Component-Specific Functions</a>
