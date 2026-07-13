---
UID: NF:msi.MsiGetComponentPathW
title: MsiGetComponentPathW function (msi.h)
description: The MsiGetComponentPath function returns the full path to an installed component. If the key path for the component is a registry key then the registry key is returned. (Unicode)
helpviewer_keywords: ["HKEY_CLASSES_ROOT", "HKEY_CURRENT_USER", "HKEY_LOCAL_MACHINE", "HKEY_USERS", "MsiGetComponentPath", "MsiGetComponentPath function", "MsiGetComponentPathW", "_msi_msigetcomponentpath", "msi/MsiGetComponentPath", "msi/MsiGetComponentPathW", "setup.msigetcomponentpath"]
old-location: setup\msigetcomponentpath.htm
tech.root: setup
ms.assetid: 957fd25c-8db6-4f2e-a705-1e8c3b3de6c1
ms.date: 12/05/2018
ms.keywords: HKEY_CLASSES_ROOT, HKEY_CURRENT_USER, HKEY_LOCAL_MACHINE, HKEY_USERS, MsiGetComponentPath, MsiGetComponentPath function, MsiGetComponentPathA, MsiGetComponentPathW, _msi_msigetcomponentpath, msi/MsiGetComponentPath, msi/MsiGetComponentPathA, msi/MsiGetComponentPathW, setup.msigetcomponentpath
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiGetComponentPathW (Unicode) and MsiGetComponentPathA (ANSI)
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
 - MsiGetComponentPathW
 - msi/MsiGetComponentPathW
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
 - MsiGetComponentPath
 - MsiGetComponentPathA
 - MsiGetComponentPathW
---

# MsiGetComponentPathW function


## -description

The 
<b>MsiGetComponentPath</b> function returns the full path to an installed component. If the key path for the component is a registry key then the registry key is returned.

## -parameters

### -param szProduct [in]

Specifies the product code for the client product.

### -param szComponent [in]

Specifies the component ID of the component to be located.

### -param lpPathBuf [out]

Pointer to a variable that receives the path to the component. This parameter can be null. If the component is a registry key, the registry roots are represented numerically. If this is a registry subkey path, there is a backslash at the end of the Key Path. If this is a registry value key path, there is no backslash at the end. For example, a registry path on a 32-bit operating system of <b>HKEY_CURRENT_USER</b>&#92;<b>SOFTWARE</b>&#92;<b>Microsoft</b> is returned as "01:\SOFTWARE\Microsoft\". The registry roots returned on 32-bit operating systems are defined as shown in the following table. 




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

### -param pcchBuf [in, out]

Pointer to a variable that specifies the size, in characters, of the buffer pointed to by the <i>lpPathBuf</i> parameter. On input, this is the full size of the buffer, including a space for a terminating null character. If the buffer passed in is too small, the count returned does not include the terminating null character. 




If <i>lpPathBuf</i> is null, <i>pcchBuf</i> can be null.

## -returns

The 
<b>MsiGetComponentPath</b> function returns the following values.
					

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
</table>

## -remarks

Upon success of the 
<b>MsiGetComponentPath</b> function, the <i>pcchBuf</i> parameter contains the length of the string in <i>lpPathBuf</i>.

The 
<b>MsiGetComponentPath</b> function might return INSTALLSTATE_ABSENT or INSTALL_STATE_UNKNOWN, for the following reasons:

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
> The msi.h header defines MsiGetComponentPath as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">Component-Specific Functions</a>
