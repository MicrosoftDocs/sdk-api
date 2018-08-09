---
UID: NF:msi.MsiAdvertiseProductW
title: MsiAdvertiseProductW function
author: windows-sdk-content
description: The MsiAdvertiseProduct function generates an advertise script or advertises a product to the computer.
old-location: setup\msiadvertiseproduct.htm
old-project: msi
ms.assetid: b28736cb-7097-4f6e-a158-a525a32d9b58
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ADVERTISEFLAGS_MACHINEASSIGN, ADVERTISEFLAGS_USERASSIGN, MsiAdvertiseProduct, MsiAdvertiseProduct function, MsiAdvertiseProductA, MsiAdvertiseProductW, _msi_msiadvertiseproduct, msi/MsiAdvertiseProduct, msi/MsiAdvertiseProductA, msi/MsiAdvertiseProductW, setup.msiadvertiseproduct
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
req.unicode-ansi: MsiAdvertiseProductW (Unicode) and MsiAdvertiseProductA (ANSI)
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
 - MsiAdvertiseProduct
 - MsiAdvertiseProductA
 - MsiAdvertiseProductW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiAdvertiseProductW function


## -description


The 
<b>MsiAdvertiseProduct</b> function generates an advertise script or advertises a product to the computer. The 
<b>MsiAdvertiseProduct</b> function enables the installer to write to a script the registry and shortcut information used to assign or publish a product. The script can be written to be consistent with a specified platform by using 
<a href="https://msdn.microsoft.com/27e8deb6-912f-4103-97a6-ec505340dccc">MsiAdvertiseProductEx</a>.


## -parameters




### -param szPackagePath [in]

The full path to the package of the product being advertised.


### -param szScriptfilePath [in]

The full path to script file that will be created with the advertise information. To advertise the product locally to the computer, set ADVERTISEFLAGS_MACHINEASSIGN or ADVERTISEFLAGS_USERASSIGN. 



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
Set to advertise a per-machine installation of the product available to all users.

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

A semicolon-delimited list of transforms to be applied. The list of transforms can be prefixed with the @ or | character to specify the secure caching of transforms. The @ prefix specifies secure-at-source transforms and the | prefix indicates secure full path transforms. For more information, see 
<a href="https://msdn.microsoft.com/c6019b28-b0a7-4104-9d78-b4b4228635b8">Secured Transforms</a>. This parameter may be null.


### -param lgidLanguage [in]

The installation language to use if the source supports multiple languages.


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
The function completed successfully.

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
An initialization error occurred.

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
 




## -see-also




<a href="https://msdn.microsoft.com/c4a0f4d8-818d-4e60-908b-adaa2a54de95">Multiple-Package Installations</a>
 

 

