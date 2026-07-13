---
UID: NF:msi.MsiAdvertiseProductW
title: MsiAdvertiseProductW function (msi.h)
description: The MsiAdvertiseProduct function generates an advertise script or advertises a product to the computer. (Unicode)
helpviewer_keywords: ["ADVERTISEFLAGS_MACHINEASSIGN", "ADVERTISEFLAGS_USERASSIGN", "MsiAdvertiseProduct", "MsiAdvertiseProduct function", "MsiAdvertiseProductW", "_msi_msiadvertiseproduct", "msi/MsiAdvertiseProduct", "msi/MsiAdvertiseProductW", "setup.msiadvertiseproduct"]
old-location: setup\msiadvertiseproduct.htm
tech.root: setup
ms.assetid: b28736cb-7097-4f6e-a158-a525a32d9b58
ms.date: 12/05/2018
ms.keywords: ADVERTISEFLAGS_MACHINEASSIGN, ADVERTISEFLAGS_USERASSIGN, MsiAdvertiseProduct, MsiAdvertiseProduct function, MsiAdvertiseProductA, MsiAdvertiseProductW, _msi_msiadvertiseproduct, msi/MsiAdvertiseProduct, msi/MsiAdvertiseProductA, msi/MsiAdvertiseProductW, setup.msiadvertiseproduct
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
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiAdvertiseProductW
 - msi/MsiAdvertiseProductW
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
 - MsiAdvertiseProduct
 - MsiAdvertiseProductA
 - MsiAdvertiseProductW
---

# MsiAdvertiseProductW function


## -description

The 
<b>MsiAdvertiseProduct</b> function generates an advertise script or advertises a product to the computer. The 
<b>MsiAdvertiseProduct</b> function enables the installer to write to a script the registry and shortcut information used to assign or publish a product. The script can be written to be consistent with a specified platform by using 
<a href="/windows/desktop/api/msi/nf-msi-msiadvertiseproductexa">MsiAdvertiseProductEx</a>.

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
<a href="/windows/desktop/Msi/secured-transforms">Secured Transforms</a>. This parameter may be null.

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

<a href="/windows/desktop/Msi/multiple-package-installations">Multiple-Package Installations</a>

## -remarks

> [!NOTE]
> The msi.h header defines MsiAdvertiseProduct as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
