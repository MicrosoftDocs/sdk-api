---
UID: NF:msi.MsiUseFeatureExA
title: MsiUseFeatureExA function
author: windows-sdk-content
description: The MsiUseFeatureEx function increments the usage count for a particular feature and indicates the installation state for that feature. This function should be used to indicate an application's intent to use a feature.
old-location: setup\msiusefeatureex.htm
tech.root: msi
ms.assetid: fa05124c-e1ed-4059-9af3-2a914785799d
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: INSTALLMODE_NODETECTION, MsiUseFeatureEx, MsiUseFeatureEx function, MsiUseFeatureExA, MsiUseFeatureExW, _msi_msiusefeatureex, msi/MsiUseFeatureEx, msi/MsiUseFeatureExA, msi/MsiUseFeatureExW, setup.msiusefeatureex
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
req.unicode-ansi: MsiUseFeatureExW (Unicode) and MsiUseFeatureExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiUseFeatureEx
 - MsiUseFeatureExA
 - MsiUseFeatureExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MsiUseFeatureExA function


## -description


The 
<b>MsiUseFeatureEx</b> function increments the usage count for a particular feature and indicates the installation state for that feature. This function should be used to indicate an application's intent to use a feature.


## -parameters




### -param szProduct [in]

Specifies the product code for the product that owns the feature to be used.


### -param szFeature [in]

Identifies the feature to be used.


### -param dwInstallMode [in]

This parameter can have the following value. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLMODE_NODETECTION"></a><a id="installmode_nodetection"></a><dl>
<dt><b>INSTALLMODE_NODETECTION</b></dt>
</dl>
</td>
<td width="60%">
Return value indicates the installation state.

</td>
</tr>
</table>
 


### -param dwReserved [in]

Reserved for future use. This value must be set to 0.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_ABSENT</b></dt>
</dl>
</td>
<td width="60%">
The feature is not installed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_ADVERTISED</b></dt>
</dl>
</td>
<td width="60%">
The feature is advertised

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
The feature is locally installed and available for use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_SOURCE</b></dt>
</dl>
</td>
<td width="60%">
The feature is installed from the source and available for use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The feature is not published.

</td>
</tr>
</table>
 




## -remarks



The 
<b>MsiUseFeatureEx</b> function should only be used on features known to be published. INSTALLSTATE_UNKNOWN indicates that the program is trying to use a feature that is not published. The application should determine whether the feature is published before calling 
<a href="https://msdn.microsoft.com/7a4dc671-d82e-4775-8198-79b80a4dd9e4">MsiUseFeature</a> by calling 
<a href="https://msdn.microsoft.com/d84aa7f1-d29a-493d-a065-8f7b680019d7">MsiQueryFeatureState</a> or 
<a href="https://msdn.microsoft.com/0ac6fea4-cdc8-4799-9001-f9399b22e7a5">MsiEnumFeatures</a>. The application should make these calls while it initializes. An application should only use features that are known to be published.




## -see-also




<a href="https://msdn.microsoft.com/05a16915-6b47-4d51-b62a-5a4d92b87e50">Application-Only Functions</a>
 

 

