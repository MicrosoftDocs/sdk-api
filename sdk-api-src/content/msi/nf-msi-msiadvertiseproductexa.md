---
UID: NF:msi.MsiAdvertiseProductExA
title: MsiAdvertiseProductExA function
author: windows-sdk-content
description: The MsiAdvertiseProductEx function generates an advertise script or advertises a product to the computer.
old-location: setup\msiadvertiseproductex.htm
old-project: Msi
ms.assetid: 27e8deb6-912f-4103-97a6-ec505340dccc
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: ADVERTISEFLAGS_MACHINEASSIGN, ADVERTISEFLAGS_USERASSIGN, MSIADVERTISEOPTIONS_INSTANCE, MSIARCHITECTUREFLAGS_AMD64, MSIARCHITECTUREFLAGS_IA64, MSIARCHITECTUREFLAGS_X86, MsiAdvertiseProductEx, MsiAdvertiseProductEx function, MsiAdvertiseProductExA, MsiAdvertiseProductExW, _msi_msiadvertiseproductex, msi/MsiAdvertiseProductEx, msi/MsiAdvertiseProductExA, msi/MsiAdvertiseProductExW, none, setup.msiadvertiseproductex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: DRM_LICENSE_ACQ_DATA
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
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiAdvertiseProductExA function


## -description


The 
<b>MsiAdvertiseProductEx</b> function generates an advertise script or advertises a product to the computer. This 
function enables Windows Installer to write to a script  the registry and shortcut information used to assign or publish a product. The script can be written to be consistent with a specified platform by using 
<b>MsiAdvertiseProductEx</b>. The <b>MsiAdvertiseProductEx</b> function provides the same functionality as 
<a href="https://msdn.microsoft.com/b28736cb-7097-4f6e-a158-a525a32d9b58">MsiAdvertiseProduct</a>. 


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
<a href="https://msdn.microsoft.com/c6019b28-b0a7-4104-9d78-b4b4228635b8">Secured Transforms</a>. This parameter may be null.


### -param lgidLanguage [in]

The language to use if the source supports multiple languages.


### -param dwPlatform [in]

Bit flags that control for which platform the installer should create the script. This parameter is ignored if <i>szScriptfilePath</i> is null. If <i>dwPlatform</i> is zero (0), then the script is created based on the current platform. This is the same functionality as 
<a href="https://msdn.microsoft.com/b28736cb-7097-4f6e-a158-a525a32d9b58">MsiAdvertiseProduct</a>. If <i>dwPlatform</i> is 1 or 2, the installer creates script for the specified platform. 



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
Multiple instances through product code changing transform support flag. Advertises a new instance of the product. Requires that the <i>szTransforms</i> parameter includes the instance transform that changes the product code. For more information, see <a href="https://msdn.microsoft.com/5147ecbd-c395-4a8f-972d-f5c5b2173eff">Installing Multiple Instances of Products and Patches</a>.

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




## -see-also




<a href="https://msdn.microsoft.com/c4a0f4d8-818d-4e60-908b-adaa2a54de95">Multiple-Package Installations</a>



<a href="https://msdn.microsoft.com/850b598a-338e-4f84-8336-01e962256a08">Not Supported in Windows Installer 2.0 and earlier</a>
 

 

