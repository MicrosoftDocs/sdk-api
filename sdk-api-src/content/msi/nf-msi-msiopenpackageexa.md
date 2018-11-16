---
UID: NF:msi.MsiOpenPackageExA
title: MsiOpenPackageExA function
author: windows-sdk-content
description: The MsiOpenPackageEx function opens a package to use with functions that access the product database.
old-location: setup\msiopenpackageex.htm
tech.root: Msi
ms.assetid: 9e9550e9-9c10-4ef1-a172-dfacaaa37fd0
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: MSIOPENPACKAGEFLAGS_IGNOREMACHINESTATE, MsiOpenPackageEx, MsiOpenPackageEx function, MsiOpenPackageExA, MsiOpenPackageExW, _msi_msiopenpackageex, msi/MsiOpenPackageEx, msi/MsiOpenPackageExA, msi/MsiOpenPackageExW, setup.msiopenpackageex
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
req.unicode-ansi: MsiOpenPackageExW (Unicode) and MsiOpenPackageExA (ANSI)
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
 - MsiOpenPackageEx
 - MsiOpenPackageExA
 - MsiOpenPackageExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- MsiOpenPackageExA
: 
---

# MsiOpenPackageExA function


## -description


The 
<b>MsiOpenPackageEx</b> function opens a package to use with functions that access the product database. The 
<a href="https://msdn.microsoft.com/b9e90ed4-fda8-4628-a713-67c651e1b572">MsiCloseHandle</a> function must be called with the handle when the handle is no longer needed.<div class="alert"><b>Note</b>  Initialize COM on the same thread before calling the <a href="https://msdn.microsoft.com/1227493a-58dc-4e41-b6d7-9ecce0b3df40">MsiOpenPackage</a>, <b>MsiOpenPackageEx</b>, or <a href="https://msdn.microsoft.com/fdc5a2f5-c44a-4cb3-b206-a598bd60024b">MsiOpenProduct</a> function.</div>
<div> </div>



## -parameters




### -param szPackagePath [in]

The path to the package.


### -param dwOptions [in]

The bit flags to indicate whether or not to ignore the computer state. Pass in 0 (zero) to use 
<a href="https://msdn.microsoft.com/1227493a-58dc-4e41-b6d7-9ecce0b3df40">MsiOpenPackage</a> behavior. 



<table>
<tr>
<th>Constant</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSIOPENPACKAGEFLAGS_IGNOREMACHINESTATE"></a><a id="msiopenpackageflags_ignoremachinestate"></a><dl>
<dt><b>MSIOPENPACKAGEFLAGS_IGNOREMACHINESTATE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Ignore the computer state when creating the product handle.

</td>
</tr>
</table>
 


### -param hProduct [out]

A pointer to a variable that receives the product handle.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_CONFIGURATION</b></dt>
</dl>
</td>
<td width="60%">
The configuration information is corrupt.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The product could not be opened.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_REMOTE_PROHIBITED</b></dt>
</dl>
</td>
<td width="60%">
Windows Installer does not permit installation from a remote desktop connection.

</td>
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
The function completes successfully.

</td>
</tr>
</table>
 

If this function fails, it may return a system error code. For more information, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



To create a restricted product handle that is independent of the current machine state and incapable of changing the current machine state, use 
<b>MsiOpenPackageEx</b> with MSIOPENPACKAGEFLAGS_IGNOREMACHINESTATE set in <i>dwOptions</i>.

Note that if <i>dwOptions</i> is MSIOPENPACKAGEFLAGS_IGNOREMACHINESTATE or 1, 
<b>MsiOpenPackageEx</b> ignores the current machine state when creating the product handle. If the value of <i>dwOptions</i> is 0, 
<b>MsiOpenPackageEx</b> is the same as 
<a href="https://msdn.microsoft.com/1227493a-58dc-4e41-b6d7-9ecce0b3df40">MsiOpenPackage</a> and creates a product handle that is dependent upon whether the package specified by <i>szPackagePath</i> is already installed on the computer.

The restricted handle created by using 
<b>MsiOpenPackageEx</b> with MSIOPENPACKAGEFLAGS_IGNOREMACHINESTATE only permits execution of dialogs, a subset of the standard actions, and custom actions that set properties (
<a href="https://msdn.microsoft.com/b88b5f48-5353-4876-9dda-2eeda288fa4b">Custom Action Type 35</a>, 
<a href="https://msdn.microsoft.com/cdad16ad-426c-4e04-8003-b32c67be7329">Custom Action Type 51</a>, and 
<a href="https://msdn.microsoft.com/c6df5462-e20e-4486-8480-8c747193c5d9">Custom Action Type 19</a>). The restricted handle prevents the use of custom actions that run 
<a href="https://msdn.microsoft.com/605c7b97-70bd-467a-9438-47b05d8b6b5d">Dynamic-Link Libraries</a>, 
<a href="https://msdn.microsoft.com/28416230-d0c2-4f6a-9908-45851a5664c5">Executable Files</a> or 
<a href="https://msdn.microsoft.com/d859713f-b8b8-4eb0-b678-52b5d880bd20">Scripts</a>.

You can call 
<a href="https://msdn.microsoft.com/33f2de47-71ab-4da8-bd56-ee58cde86e2b">MsiDoAction</a> on the following standard actions using the restricted handle. All other actions return ERROR_FUNCTION_NOT_CALLED if called with the restricted handle.

<ul>
<li>
<a href="https://msdn.microsoft.com/9925a645-5909-42c7-9de8-f908a5e42be9">ADMIN</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d9c843e4-fcd9-4d47-9ca9-ffa83ed80574">ADVERTISE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/bf290b59-1ecb-410f-b1f6-fdbeebebe3d3">INSTALL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1393bfaa-8649-40d3-9ff8-5e119c34aed3">SEQUENCE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/56665876-2c74-476b-aa1a-158c6e86418d">AppSearch action</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0aa7bf8b-de76-464d-8e7b-3aa4f609fe19">CCPSearch</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ae69ad03-5acc-4a62-ba71-3a4e477d34ab">CostFinalize</a>
</li>
<li>
<a href="https://msdn.microsoft.com/be9a8382-c892-44ae-8b59-c665b5cca2d2">CostInitialize</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1b3f2baf-6191-452e-955d-8ac903edc1b7">FileCost</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7efcb767-9bdf-43a4-83b8-61b6fc84adf6">FindRelatedProducts</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3f39ad5d-5539-48cc-8369-bd4d3127fbdd">IsolateComponents action</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b356987d-3efe-4a57-a745-91a1b34222e9">LaunchConditions</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3f53c555-02a9-4249-9f1a-98cd655fc79f">MigrateFeatureStates</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6d6205a0-a870-4df2-922b-befea7e28a1a">ResolveSource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d37b2434-86eb-4c6e-b817-77c75dcebbf5">RMCCPSearch</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31b2f9d2-98d5-4cf3-af02-f12de2740bb8">ValidateProductID</a>
</li>
</ul>
The 
<a href="https://msdn.microsoft.com/b9e90ed4-fda8-4628-a713-67c651e1b572">MsiCloseHandle</a> function must be called when the handle is not needed.



