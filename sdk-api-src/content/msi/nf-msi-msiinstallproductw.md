---
UID: NF:msi.MsiInstallProductW
title: MsiInstallProductW function
author: windows-sdk-content
description: Installs or uninstalls a product.
old-location: setup\msiinstallproduct.htm
old-project: msi
ms.assetid: ec8d6710-ecfe-432c-ba1d-2e3532a25988
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: MsiInstallProduct, MsiInstallProduct function, MsiInstallProductA, MsiInstallProductW, _msi_msiinstallproduct, msi/MsiInstallProduct, msi/MsiInstallProductA, msi/MsiInstallProductW, setup.msiinstallproduct
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiInstallProductW (Unicode) and MsiInstallProductA (ANSI)
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
 - Ext-MS-Win-MSi-Misc-L1-1-0.dll
api_name:
 - MsiInstallProduct
 - MsiInstallProductA
 - MsiInstallProductW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiInstallProductW function


## -description


The 
<b>MsiInstallProduct</b> function installs or uninstalls a product.


## -parameters




### -param szPackagePath [in]

A null-terminated string that specifies the path to the location of the Windows Installer package. The string value can contain a URL (e.g. <code>http://packageLocation/package/package.msi</code>), a network path  (e.g. \\packageLocation\package.msi), a file path (e.g. file://packageLocation/package.msi), or a local path (e.g. D:\packageLocation\package.msi).


### -param szCommandLine [in]

A null-terminated string that specifies the command line property settings. This should be a list of the format <i>Property=Setting Property=Setting</i>. For more information, see 
<a href="https://msdn.microsoft.com/b7b715e7-e92c-4b84-b60d-a0ff8412749b">About Properties</a>.

To perform an administrative installation, include ACTION=ADMIN in <i>szCommandLine</i>. For more information, see the 
<a href="https://msdn.microsoft.com/library/windows/hardware/mt270124">ACTION</a> property.


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
<dt><b>An error relating to an action</b></dt>
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
An error that relates to initialization occurred.

</td>
</tr>
</table>
 

For more information, see 
<a href="https://msdn.microsoft.com/0153a21f-9b26-4088-b12b-96c9e6918cc3">Displayed Error Messages</a>.




## -remarks



The 
<b>MsiInstallProduct</b> function displays the user interface with the current settings and log mode.

<ul>
<li>You can change user interface settings by using the 
<a href="https://msdn.microsoft.com/303c2ea9-4c8f-46d3-b587-7c50e2810c28">MsiSetInternalUI</a>, 
<a href="https://msdn.microsoft.com/fcbf0607-d048-486f-bec2-f6e9d03e4194">MsiSetExternalUI</a>, or <a href="https://msdn.microsoft.com/f2cd2bb7-0e4f-4d3b-9e6c-6f15661064df">MsiSetExternalUIRecord</a> functions.</li>
<li>You can set the log mode by using the 
<a href="https://msdn.microsoft.com/117ccd0b-e434-453f-9602-ff50bc85db6e">MsiEnableLog</a> function.</li>
<li>You can completely remove a product by setting REMOVE=ALL in <i>szCommandLine</i>.</li>
</ul>
For more information, see 
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">REMOVE</a> Property.




## -see-also




<a href="https://msdn.microsoft.com/0153a21f-9b26-4088-b12b-96c9e6918cc3">Displayed Error Messages</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>



<a href="https://msdn.microsoft.com/5cce27ff-1143-4fe6-b4bd-727581431c07">Initialization Error</a>



<a href="https://msdn.microsoft.com/05a16915-6b47-4d51-b62a-5a4d92b87e50">Installation and Configuration Functions</a>



<a href="https://msdn.microsoft.com/c4a0f4d8-818d-4e60-908b-adaa2a54de95">Multiple-Package Installations</a>
 

 

