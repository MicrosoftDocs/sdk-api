---
UID: NF:msi.MsiQueryFeatureStateW
title: MsiQueryFeatureStateW function
author: windows-sdk-content
description: The MsiQueryFeatureState function returns the installed state for a product feature.
old-location: setup\msiqueryfeaturestate.htm
old-project: msi
ms.assetid: d84aa7f1-d29a-493d-a065-8f7b680019d7
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: MsiQueryFeatureState, MsiQueryFeatureState function, MsiQueryFeatureStateA, MsiQueryFeatureStateW, _msi_msiqueryfeaturestate, msi/MsiQueryFeatureState, msi/MsiQueryFeatureStateA, msi/MsiQueryFeatureStateW, setup.msiqueryfeaturestate
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
req.unicode-ansi: MsiQueryFeatureStateW (Unicode) and MsiQueryFeatureStateA (ANSI)
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
 - MsiQueryFeatureState
 - MsiQueryFeatureStateA
 - MsiQueryFeatureStateW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiQueryFeatureStateW function


## -description


The 
<b>MsiQueryFeatureState</b> function returns the installed state for a product feature.


## -parameters




### -param szProduct [in]

Specifies the product code for the product that contains the feature of interest.


### -param szFeature [in]

Identifies the feature of interest.


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
The feature is installed locally.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_SOURCE</b></dt>
</dl>
</td>
<td width="60%">
The feature is installed to run from source.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The product code or feature ID is unknown.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



The 
<b>MsiQueryFeatureState</b> function does not validate that the feature is actually accessible.




## -see-also




<a href="https://msdn.microsoft.com/05a16915-6b47-4d51-b62a-5a4d92b87e50">System Status Functions</a>
 

 

