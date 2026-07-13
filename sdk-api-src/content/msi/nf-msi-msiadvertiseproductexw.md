---
UID: NF:msi.MsiAdvertiseProductExW
title: MsiAdvertiseProductExW function (msi.h)
description: The MsiAdvertiseProductEx function generates an advertise script or advertises a product to the computer. (Unicode)
helpviewer_keywords: ["ADVERTISEFLAGS_MACHINEASSIGN", "ADVERTISEFLAGS_USERASSIGN", "MSIADVERTISEOPTIONS_INSTANCE", "MSIARCHITECTUREFLAGS_AMD64", "MSIARCHITECTUREFLAGS_IA64", "MSIARCHITECTUREFLAGS_X86", "MsiAdvertiseProductEx", "MsiAdvertiseProductEx function", "MsiAdvertiseProductExW", "_msi_msiadvertiseproductex", "msi/MsiAdvertiseProductEx", "msi/MsiAdvertiseProductExW", "none", "setup.msiadvertiseproductex"]
old-location: setup\msiadvertiseproductex.htm
tech.root: setup
ms.assetid: 27e8deb6-912f-4103-97a6-ec505340dccc
ms.date: 12/05/2018
ms.keywords: ADVERTISEFLAGS_MACHINEASSIGN, ADVERTISEFLAGS_USERASSIGN, MSIADVERTISEOPTIONS_INSTANCE, MSIARCHITECTUREFLAGS_AMD64, MSIARCHITECTUREFLAGS_IA64, MSIARCHITECTUREFLAGS_X86, MsiAdvertiseProductEx, MsiAdvertiseProductEx function, MsiAdvertiseProductExA, MsiAdvertiseProductExW, _msi_msiadvertiseproductex, msi/MsiAdvertiseProductEx, msi/MsiAdvertiseProductExA, msi/MsiAdvertiseProductExW, none, setup.msiadvertiseproductex
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiAdvertiseProductExW (Unicode) and MsiAdvertiseProductExA (ANSI)
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
 - MsiAdvertiseProductExW
 - msi/MsiAdvertiseProductExW
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
 - MsiAdvertiseProductEx
 - MsiAdvertiseProductExA
 - MsiAdvertiseProductExW
---

# MsiAdvertiseProductExW function


## -description

The 
<b>MsiAdvertiseProductEx</b> function generates an advertise script or advertises a product to the computer. This 
function enables Windows Installer to write to a script  the registry and shortcut information used to assign or publish a product. The script can be written to be consistent with a specified platform by using 
<b>MsiAdvertiseProductEx</b>. The <b>MsiAdvertiseProductEx</b> function provides the same functionality as 
<a href="/windows/desktop/api/msi/nf-msi-msiadvertiseproducta">MsiAdvertiseProduct</a>.

## -parameters

### -param szPackagePath [in]

The full path to the package of the product being advertised.

### -param szScriptfilePath [in]

The full path to the script file to be created with the advertised information. To advertise the product locally to the computer, set ADVERTISEFLAGS_MACHINEASSIGN or ADVERTISEFLAGS_USERASSIGN. 



<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ADVERTISEFLAGS_MACHINEASSIGN"></a><a id="advertiseflags_machineassign"></a><dl>
<dt><b>ADVERTISEFLAGS_MACHINEASSIGN</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Set to advertise a per-computer installation of the product available to all users.

</td>
</tr>
<tr>
<td width="40%"><a id="ADVERTISEFLAGS_USERASSIGN"></a><a id="advertiseflags_userassign"></a><dl>
<dt><b>ADVERTISEFLAGS_USERASSIGN</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Set to advertise a per-user installation of the product available to a particular user.

</td>
</tr>
</table>

### -param szTransforms [in]

A semicolon–delimited list of transforms to be applied. The list of transforms can be prefixed with the @ or | character to specify the secure caching of transforms. The @ prefix specifies secure-at-source transforms and the | prefix indicates secure full path–transforms. For more information, see 
<a href="/windows/desktop/Msi/secured-transforms">Secured Transforms</a>. This parameter may be null.

### -param lgidLanguage [in]

The language to use if the source supports multiple languages.

### -param dwPlatform [in]

Bit flags that control for which platform the installer should create the script. This parameter is ignored if <i>szScriptfilePath</i> is null. If <i>dwPlatform</i> is zero (0), then the script is created based on the current platform. This is the same functionality as 
<a href="/windows/desktop/api/msi/nf-msi-msiadvertiseproducta">MsiAdvertiseProduct</a>. If <i>dwPlatform</i> is 1 or 2, the installer creates script for the specified platform. 



<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="none"></a><a id="NONE"></a><dl>
<dt><b>none</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Creates a script for the current platform.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIARCHITECTUREFLAGS_X86"></a><a id="msiarchitectureflags_x86"></a><dl>
<dt><b>MSIARCHITECTUREFLAGS_X86</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Creates a script for the x86 platform.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIARCHITECTUREFLAGS_IA64"></a><a id="msiarchitectureflags_ia64"></a><dl>
<dt><b>MSIARCHITECTUREFLAGS_IA64</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Creates a script for Itanium-based systems.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIARCHITECTUREFLAGS_AMD64"></a><a id="msiarchitectureflags_amd64"></a><dl>
<dt><b>MSIARCHITECTUREFLAGS_AMD64</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Creates a script for the x64 platform.

</td>
</tr>
</table>

### -param dwOptions [in]

Bit flags that specify extra advertisement options. Nonzero value is only available in Windows Installer versions shipped with Windows Server 2003 and Windows XP with SP1 and later.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSIADVERTISEOPTIONS_INSTANCE"></a><a id="msiadvertiseoptions_instance"></a><dl>
<dt><b>MSIADVERTISEOPTIONS_INSTANCE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Multiple instances through product code changing transform support flag. Advertises a new instance of the product. Requires that the <i>szTransforms</i> parameter includes the instance transform that changes the product code. For more information, see <a href="/windows/desktop/Msi/installing-multiple-instances-of-products-and-patches">Installing Multiple Instances of Products and Patches</a>.

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
An initialization error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CALL_NOT_IMPLEMENTED</b></dt>
</dl>
</td>
<td width="60%">
This error is returned if an attempt is made to generate an advertise script on any platform other than Windows 2000 or Windows XP. Advertisement to the local computer is supported on all platforms.

</td>
</tr>
</table>

## -remarks

Multiple instances through product code–changing transforms is only available for Windows Installer versions shipping with   Windows Server 2003  and Windows XP with SP1 and later.





> [!NOTE]
> The msi.h header defines MsiAdvertiseProductEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/multiple-package-installations">Multiple-Package Installations</a>



<a href="/windows/desktop/Msi/not-supported-in-windows-installer-version-2-0">Not Supported in Windows Installer 2.0 and earlier</a>
