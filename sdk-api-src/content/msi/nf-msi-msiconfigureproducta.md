---
UID: NF:msi.MsiConfigureProductA
title: MsiConfigureProductA function
author: windows-sdk-content
description: The MsiConfigureProduct function installs or uninstalls a product.
old-location: setup\msiconfigureproduct.htm
tech.root: msi
ms.assetid: 06f341ac-badd-47a0-af86-4fb76bf528d6
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: INSTALLLEVEL_DEFAULT, INSTALLLEVEL_MAXIMUM, INSTALLLEVEL_MINIMUM, INSTALLSTATE_ABSENT, INSTALLSTATE_ADVERTISED, INSTALLSTATE_DEFAULT, INSTALLSTATE_LOCAL, INSTALLSTATE_SOURCE, MsiConfigureProduct, MsiConfigureProduct function, MsiConfigureProductA, MsiConfigureProductW, _msi_msiconfigureproduct, msi/MsiConfigureProduct, msi/MsiConfigureProductA, msi/MsiConfigureProductW, setup.msiconfigureproduct
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
req.unicode-ansi: MsiConfigureProductW (Unicode) and MsiConfigureProductA (ANSI)
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
 - MsiConfigureProduct
 - MsiConfigureProductA
 - MsiConfigureProductW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MsiConfigureProductA function


## -description


The 
<b>MsiConfigureProduct</b> function installs or uninstalls a product.


## -parameters




### -param szProduct [in]

Specifies the product code for the product to be configured.


### -param iInstallLevel [in]

Specifies how much of the product should be installed when installing the product to its default state. The <i>iInstallLevel</i> parameter is ignored, and all features are installed, if the <i>eInstallState</i> parameter is set to any other value than INSTALLSTATE_DEFAULT. 




This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLLEVEL_DEFAULT"></a><a id="installlevel_default"></a><dl>
<dt><b>INSTALLLEVEL_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The authored default features are installed.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLEVEL_MINIMUM"></a><a id="installlevel_minimum"></a><dl>
<dt><b>INSTALLLEVEL_MINIMUM</b></dt>
</dl>
</td>
<td width="60%">
Only the required features are installed. You can specify a value between INSTALLLEVEL_MINIMUM and INSTALLLEVEL_MAXIMUM to install a subset of available features.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLEVEL_MAXIMUM"></a><a id="installlevel_maximum"></a><dl>
<dt><b>INSTALLLEVEL_MAXIMUM</b></dt>
</dl>
</td>
<td width="60%">
All features are installed. You can specify a value between INSTALLLEVEL_MINIMUM and INSTALLLEVEL_MAXIMUM to install a subset of available features.

</td>
</tr>
</table>
 


### -param eInstallState [in]

Specifies the installation state for the product. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_LOCAL"></a><a id="installstate_local"></a><dl>
<dt><b>INSTALLSTATE_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
The product is to be installed with all features installed locally.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_ABSENT"></a><a id="installstate_absent"></a><dl>
<dt><b>INSTALLSTATE_ABSENT</b></dt>
</dl>
</td>
<td width="60%">
The product is uninstalled.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_SOURCE"></a><a id="installstate_source"></a><dl>
<dt><b>INSTALLSTATE_SOURCE</b></dt>
</dl>
</td>
<td width="60%">
The product is to be installed with all features installed to run from source.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_DEFAULT"></a><a id="installstate_default"></a><dl>
<dt><b>INSTALLSTATE_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The product is to be installed with all features installed to the default states specified in the <a href="https://msdn.microsoft.com/1faee1d5-6e39-43ea-bf92-a0b3986a13a1">Feature Table</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_ADVERTISED"></a><a id="installstate_advertised"></a><dl>
<dt><b>INSTALLSTATE_ADVERTISED</b></dt>
</dl>
</td>
<td width="60%">
The product is advertised.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter is passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function succeeds.

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
<a href="https://msdn.microsoft.com/9ea81ef3-a5b5-4d13-b0b8-3da6e919315e">Error Codes</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/5cce27ff-1143-4fe6-b4bd-727581431c07">Initialization Error</a></b></dt>
</dl>
</td>
<td width="60%">
An error that relates to initialization.

</td>
</tr>
</table>
 




## -remarks



The 
<b>MsiConfigureProduct</b> function displays the user interface (UI) using the current settings. User interface settings can be changed by using 
<a href="https://msdn.microsoft.com/303c2ea9-4c8f-46d3-b587-7c50e2810c28">MsiSetInternalUI</a>, <a href="https://msdn.microsoft.com/fcbf0607-d048-486f-bec2-f6e9d03e4194">MsiSetExternalUI</a> or <a href="https://msdn.microsoft.com/f2cd2bb7-0e4f-4d3b-9e6c-6f15661064df">MsiSetExternalUIRecord</a>.

The <i>iInstallLevel</i> parameter is ignored, and all features of the product are installed, if the <i>eInstallState</i> parameter is set to any other value than INSTALLSTATE_DEFAULT. To control the installation of individual features when the <i>eInstallState</i> parameter is not set to INSTALLSTATE_DEFAULT, use 
<a href="https://msdn.microsoft.com/067d6fbb-833f-4e0e-bfdb-18d1b8608f58">MsiConfigureFeature</a>.




## -see-also




<a href="https://msdn.microsoft.com/c4a0f4d8-818d-4e60-908b-adaa2a54de95">Multiple-Package Installations</a>
 

 

