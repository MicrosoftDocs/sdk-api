---
UID: NF:msi.MsiConfigureProductExA
title: MsiConfigureProductExA function
author: windows-sdk-content
description: Installs or uninstalls a product.
old-location: setup\msiconfigureproductex.htm
tech.root: msi
ms.assetid: 7a7ae88a-b893-4d10-8542-b2066d1572a9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: INSTALLLEVEL_DEFAULT, INSTALLLEVEL_MAXIMUM, INSTALLLEVEL_MINIMUM, INSTALLSTATE_ABSENT, INSTALLSTATE_ADVERTISED, INSTALLSTATE_DEFAULT, INSTALLSTATE_LOCAL, INSTALLSTATE_SOURCE, MsiConfigureProductEx, MsiConfigureProductEx function, MsiConfigureProductExA, MsiConfigureProductExW, _msi_msiconfigureproductex, msi/MsiConfigureProductEx, msi/MsiConfigureProductExA, msi/MsiConfigureProductExW, setup.msiconfigureproductex
ms.topic: function
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiConfigureProductExW (Unicode) and MsiConfigureProductExA (ANSI)
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
 - Ext-MS-Win-MSi-Misc-L1-1-0.dll
api_name:
 - MsiConfigureProductEx
 - MsiConfigureProductExA
 - MsiConfigureProductExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MsiConfigureProductExA function


## -description


The 
<b>MsiConfigureProductEx</b> function installs or uninstalls a product. A product command line can also be specified.


## -parameters




### -param szProduct [in]

Specifies the product code for the product to be configured.


### -param iInstallLevel [in]

Specifies how much of the product should be installed when installing the product to its default state. The <i>iInstallLevel</i> parameters are ignored, and all features are installed, if the <i>eInstallState</i> parameter is set to any value other than <b>INSTALLSTATE_DEFAULT</b>.

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
Only the required features are installed. You can specify a value between <b>INSTALLLEVEL_MINIMUM</b> and <b>INSTALLLEVEL_MAXIMUM</b> to install a subset of available features.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLEVEL_MAXIMUM"></a><a id="installlevel_maximum"></a><dl>
<dt><b>INSTALLLEVEL_MAXIMUM</b></dt>
</dl>
</td>
<td width="60%">
All features are installed. You can specify a value between <b>INSTALLLEVEL_MINIMUM</b> and <b>INSTALLLEVEL_MAXIMUM</b> to install a subset of available features.

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
 


### -param szCommandLine [in]

Specifies the command-line property settings. This should be a list of the format <i>Property=Setting Property=Setting</i>. For more information, see 
<a href="https://msdn.microsoft.com/b7b715e7-e92c-4b84-b60d-a0ff8412749b">About Properties</a>.


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
The function succeeded.

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
An error relating to initialization occurred.

</td>
</tr>
</table>
 




## -remarks



The command line passed in as <i>szCommandLine</i> can contain any of the 
<a href="https://msdn.microsoft.com/c91119b9-59d5-4a33-91cd-d3ba63659d12">Feature Installation Options Properties</a>. In this case, the <i>eInstallState</i> passed must be <b>INSTALLSTATE_DEFAULT</b>.

The <i>iInstallLevel</i> parameter is ignored and all features of the product are installed if the <i>eInstallState</i> parameter is set to any other value than <b>INSTALLSTATE_DEFAULT</b>. To control the installation of individual features when the <i>eInstallState</i> parameter is not set to <b>INSTALLSTATE_DEFAULT</b> use 
<a href="https://msdn.microsoft.com/067d6fbb-833f-4e0e-bfdb-18d1b8608f58">MsiConfigureFeature</a>.

The 
<b>MsiConfigureProductEx</b> function displays the user interface using the current settings. User interface settings can be changed with 
<a href="https://msdn.microsoft.com/303c2ea9-4c8f-46d3-b587-7c50e2810c28">MsiSetInternalUI</a>, <a href="https://msdn.microsoft.com/fcbf0607-d048-486f-bec2-f6e9d03e4194">MsiSetExternalUI</a>, or <a href="https://msdn.microsoft.com/f2cd2bb7-0e4f-4d3b-9e6c-6f15661064df">MsiSetExternalUIRecord</a>.




## -see-also




<a href="https://msdn.microsoft.com/0153a21f-9b26-4088-b12b-96c9e6918cc3">Displayed Error Messages</a>



<a href="https://msdn.microsoft.com/9ea81ef3-a5b5-4d13-b0b8-3da6e919315e">Error Codes</a>



<a href="https://msdn.microsoft.com/5cce27ff-1143-4fe6-b4bd-727581431c07">Initialization Error</a>



<a href="https://msdn.microsoft.com/05a16915-6b47-4d51-b62a-5a4d92b87e50">Installation and Configuration Functions</a>



<a href="https://msdn.microsoft.com/c4a0f4d8-818d-4e60-908b-adaa2a54de95">Multiple-Package Installations</a>
 

 

