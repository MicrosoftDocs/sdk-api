---
UID: NF:msi.MsiOpenPackageExW
title: MsiOpenPackageExW function (msi.h)
description: The MsiOpenPackageEx function opens a package to use with functions that access the product database. (Unicode)
helpviewer_keywords: ["MSIOPENPACKAGEFLAGS_IGNOREMACHINESTATE", "MsiOpenPackageEx", "MsiOpenPackageEx function", "MsiOpenPackageExW", "_msi_msiopenpackageex", "msi/MsiOpenPackageEx", "msi/MsiOpenPackageExW", "setup.msiopenpackageex"]
old-location: setup\msiopenpackageex.htm
tech.root: setup
ms.assetid: 9e9550e9-9c10-4ef1-a172-dfacaaa37fd0
ms.date: 12/05/2018
ms.keywords: MSIOPENPACKAGEFLAGS_IGNOREMACHINESTATE, MsiOpenPackageEx, MsiOpenPackageEx function, MsiOpenPackageExA, MsiOpenPackageExW, _msi_msiopenpackageex, msi/MsiOpenPackageEx, msi/MsiOpenPackageExA, msi/MsiOpenPackageExW, setup.msiopenpackageex
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiOpenPackageExW
 - msi/MsiOpenPackageExW
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
 - MsiOpenPackageEx
 - MsiOpenPackageExA
 - MsiOpenPackageExW
---

# MsiOpenPackageExW function


## -description

The 
<b>MsiOpenPackageEx</b> function opens a package to use with functions that access the product database. The 
<a href="/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a> function must be called with the handle when the handle is no longer needed.<div class="alert"><b>Note</b>  Initialize COM on the same thread before calling the <a href="/windows/desktop/api/msi/nf-msi-msiopenpackagea">MsiOpenPackage</a>, <b>MsiOpenPackageEx</b>, or <a href="/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a> function.</div>
<div> </div>

## -parameters

### -param szPackagePath [in]

The path to the package.

### -param dwOptions [in]

The bit flags to indicate whether or not to ignore the computer state. Pass in 0 (zero) to use 
<a href="/windows/desktop/api/msi/nf-msi-msiopenpackagea">MsiOpenPackage</a> behavior. 



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
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

To create a restricted product handle that is independent of the current machine state and incapable of changing the current machine state, use 
<b>MsiOpenPackageEx</b> with MSIOPENPACKAGEFLAGS_IGNOREMACHINESTATE set in <i>dwOptions</i>.

Note that if <i>dwOptions</i> is MSIOPENPACKAGEFLAGS_IGNOREMACHINESTATE or 1, 
<b>MsiOpenPackageEx</b> ignores the current machine state when creating the product handle. If the value of <i>dwOptions</i> is 0, 
<b>MsiOpenPackageEx</b> is the same as 
<a href="/windows/desktop/api/msi/nf-msi-msiopenpackagea">MsiOpenPackage</a> and creates a product handle that is dependent upon whether the package specified by <i>szPackagePath</i> is already installed on the computer.

The restricted handle created by using 
<b>MsiOpenPackageEx</b> with MSIOPENPACKAGEFLAGS_IGNOREMACHINESTATE only permits execution of dialogs, a subset of the standard actions, and custom actions that set properties (
<a href="/windows/desktop/Msi/custom-action-type-35">Custom Action Type 35</a>, 
<a href="/windows/desktop/Msi/custom-action-type-51">Custom Action Type 51</a>, and 
<a href="/windows/desktop/Msi/custom-action-type-19">Custom Action Type 19</a>). The restricted handle prevents the use of custom actions that run 
<a href="/windows/desktop/Msi/dynamic-link-libraries">Dynamic-Link Libraries</a>, 
<a href="/windows/desktop/Msi/executable-files">Executable Files</a> or 
<a href="/windows/desktop/Msi/scripts">Scripts</a>.

You can call 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msidoactiona">MsiDoAction</a> on the following standard actions using the restricted handle. All other actions return ERROR_FUNCTION_NOT_CALLED if called with the restricted handle.

<ul>
<li>
<a href="/windows/desktop/Msi/admin-action">ADMIN</a>
</li>
<li>
<a href="/windows/desktop/Msi/advertise-action">ADVERTISE</a>
</li>
<li>
<a href="/windows/desktop/Msi/install-action">INSTALL</a>
</li>
<li>
<a href="/windows/desktop/Msi/sequence-action">SEQUENCE</a>
</li>
<li>
<a href="/windows/desktop/Msi/appsearch-action">AppSearch action</a>
</li>
<li>
<a href="/windows/desktop/Msi/ccpsearch-action">CCPSearch</a>
</li>
<li>
<a href="/windows/desktop/Msi/costfinalize-action">CostFinalize</a>
</li>
<li>
<a href="/windows/desktop/Msi/costinitialize-action">CostInitialize</a>
</li>
<li>
<a href="/windows/desktop/Msi/filecost-action">FileCost</a>
</li>
<li>
<a href="/windows/desktop/Msi/findrelatedproducts-action">FindRelatedProducts</a>
</li>
<li>
<a href="/windows/desktop/Msi/isolatecomponents-action">IsolateComponents action</a>
</li>
<li>
<a href="/windows/desktop/Msi/launchconditions-action">LaunchConditions</a>
</li>
<li>
<a href="/windows/desktop/Msi/migratefeaturestates-action">MigrateFeatureStates</a>
</li>
<li>
<a href="/windows/desktop/Msi/resolvesource-action">ResolveSource</a>
</li>
<li>
<a href="/windows/desktop/Msi/rmccpsearch-action">RMCCPSearch</a>
</li>
<li>
<a href="/windows/desktop/Msi/validateproductid-action">ValidateProductID</a>
</li>
</ul>
The 
<a href="/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a> function must be called when the handle is not needed.




> [!NOTE]
> The msi.h header defines MsiOpenPackageEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
