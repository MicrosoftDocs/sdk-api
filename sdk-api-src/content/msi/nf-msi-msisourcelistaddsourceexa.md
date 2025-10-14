---
UID: NF:msi.MsiSourceListAddSourceExA
title: MsiSourceListAddSourceExA function (msi.h)
description: Adds or reorders the set of sources of a patch or product in a specified context. It can also create a source list for a patch that does not exist in the specified context. (ANSI)
helpviewer_keywords: ["MSICODE_PATCH", "MSICODE_PRODUCT", "MSIINSTALLCONTEXT_MACHINE", "MSIINSTALLCONTEXT_USERMANAGED", "MSIINSTALLCONTEXT_USERUNMANAGED", "MSISOURCETYPE_NETWORK", "MSISOURCETYPE_URL", "MsiSourceListAddSourceExA", "NULL", "User SID", "msi/MsiSourceListAddSourceExA"]
old-location: setup\msisourcelistaddsourceex.htm
tech.root: setup
ms.assetid: 79f1286e-e30b-4989-a631-f2bcb87486a2
ms.date: 12/05/2018
ms.keywords: MSICODE_PATCH, MSICODE_PRODUCT, MSIINSTALLCONTEXT_MACHINE, MSIINSTALLCONTEXT_USERMANAGED, MSIINSTALLCONTEXT_USERUNMANAGED, MSISOURCETYPE_NETWORK, MSISOURCETYPE_URL, MsiSourceListAddSourceEx, MsiSourceListAddSourceEx function, MsiSourceListAddSourceExA, MsiSourceListAddSourceExW, NULL, User SID, msi/MsiSourceListAddSourceEx, msi/MsiSourceListAddSourceExA, msi/MsiSourceListAddSourceExW, setup.msisourcelistaddsourceex
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiSourceListAddSourceExW (Unicode) and MsiSourceListAddSourceExA (ANSI)
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
 - MsiSourceListAddSourceExA
 - msi/MsiSourceListAddSourceExA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
 - Ext-MS-Win-MSi-Misc-L1-1-0.dll
api_name:
 - MsiSourceListAddSourceEx
 - MsiSourceListAddSourceExA
 - MsiSourceListAddSourceExW
---

# MsiSourceListAddSourceExA function


## -description

The <b>MsiSourceListAddSourceEx</b> function  adds  or reorders the set of sources of a patch or product in a specified context.  It can also create a source list for a patch that does not exist in the specified context.

## -parameters

### -param szProductCodeOrPatchCode [in]

The <a href="/windows/desktop/Msi/productcode">ProductCode</a> or patch GUID of the product or patch. Use a null-terminated string. If the string is longer than 39 characters, the function fails and returns <b>ERROR_INVALID_PARAMETER</b>. This parameter cannot be <b>NULL</b>.

### -param szUserSid [in, optional]

This parameter can be a string SID that specifies the user account that contains the product or patch.  The SID is not validated or resolved. An incorrect SID can return <b>ERROR_UNKNOWN_PRODUCT</b> or <b>ERROR_UNKNOWN_PATCH</b>. When referencing a machine context, <i>szUserSID</i> must be <b>NULL</b> and <i>dwContext</i> must be <b>MSIINSTALLCONTEXT_MACHINE</b>.

<table>
<tr>
<th>Type of SID</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NULL"></a><a id="null"></a><dl>
<dt><b>NULL</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> denotes the currently logged on user.  When referencing the current user account, <i>szUserSID</i> can be <b>NULL</b> and <i>dwContext</i> can be  <b>MSIINSTALLCONTEXT_USERMANAGED</b> or <b>MSIINSTALLCONTEXT_USERUNMANAGED</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="User_SID"></a><a id="user_sid"></a><a id="USER_SID"></a><dl>
<dt><b>User SID</b></dt>
</dl>
</td>
<td width="60%">
Specifies enumeration for a particular user in the system.  An example of a user SID is "S-1-3-64-2415071341-1358098788-3127455600-2561".

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  The special SID string s-1-5-18 (system) cannot be used to enumerate products or patches installed as per-machine.  Setting the SID value to "S-1-5-18" returns <b>ERROR_INVALID_PARAMETER</b>.</div>
<div> </div>
<div class="alert"><b>Note</b>  The special SID string s-1-1-0 (everyone) should not be used. Setting the SID value to "S-1-1-0" fails and returns <b>ERROR_INVALID_PARAM</b>.</div>
<div> </div>

### -param dwContext [in]

This parameter specifies the context of the product or patch instance. This parameter can contain one of the following values.

<table>
<tr>
<th>Type of context</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERMANAGED"></a><a id="msiinstallcontext_usermanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERMANAGED</b></dt>
</dl>
</td>
<td width="60%">
The product or patch instance exists in the per-user-managed context.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERUNMANAGED"></a><a id="msiinstallcontext_userunmanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERUNMANAGED</b></dt>
</dl>
</td>
<td width="60%">
The product or patch instance exists in the  per-user-unmanaged context.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_MACHINE"></a><a id="msiinstallcontext_machine"></a><dl>
<dt><b>MSIINSTALLCONTEXT_MACHINE</b></dt>
</dl>
</td>
<td width="60%">
The product or patch instance exists in the per-machine context.

</td>
</tr>
</table>

### -param dwOptions [in]

The <i>dwOptions</i> value determines the interpretation of the <i>szProductCodeOrPatchCode</i> value and the type of sources to clear. This parameter must be a combination of one of the following <b>MSISOURCETYPE_*</b> constants and one of the following <b>MSICODE_*</b> constants.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSISOURCETYPE_NETWORK"></a><a id="msisourcetype_network"></a><dl>
<dt><b>MSISOURCETYPE_NETWORK</b></dt>
</dl>
</td>
<td width="60%">
The  source  is  a network type.

</td>
</tr>
<tr>
<td width="40%"><a id="MSISOURCETYPE_URL"></a><a id="msisourcetype_url"></a><dl>
<dt><b>MSISOURCETYPE_URL</b></dt>
</dl>
</td>
<td width="60%">
The source is a URL type.

</td>
</tr>
<tr>
<td width="40%"><a id="MSICODE_PRODUCT"></a><a id="msicode_product"></a><dl>
<dt><b>MSICODE_PRODUCT</b></dt>
</dl>
</td>
<td width="60%">
<i>szProductCodeOrPatchCode</i> is a product code.

</td>
</tr>
<tr>
<td width="40%"><a id="MSICODE_PATCH"></a><a id="msicode_patch"></a><dl>
<dt><b>MSICODE_PATCH</b></dt>
</dl>
</td>
<td width="60%">
<i>szProductCodeOrPatchCode</i> is a patch code.

</td>
</tr>
</table>

### -param szSource [in]

Source to add or move. This parameter is expected to contain only the path without the filename. 
The filename is already registered as "PackageName" and can be manipulated through <a href="/windows/desktop/api/msi/nf-msi-msisourcelistsetinfoa">MsiSourceListSetInfo</a>. This argument is required.

### -param dwIndex [in, optional]

This parameter provides the new index for the source. All sources are indexed in the source list from 1 to <i>N</i>, where <i>N</i> is the count of sources in the list. Every source in the list has a unique index.

If <b>MsiSourceListAddSourceEx</b> is called with a new source  and <i>dwIndex</i> set to 0 (zero), the new source is appended to the existing list. If <i>dwIndex</i> is set to 0 and the source already exists in the list, no update is done on the list.

If <b>MsiSourceListAddSourceEx</b> is called with a new source  and <i>dwIndex</i> set to a  non-zero value less than count (<i>N</i>), the new source is placed at the specified index and the other sources  are re-indexed. If the source already exists, it is moved to the specified index and the other sources are re-indexed.

If <b>MsiSourceListAddSourceEx</b> is called with a new source  and <i>dwIndex</i> set to a  non-zero value greater than the count of sources (<i>N</i>), the new source is appended to the existing list.  If the source already exists, it is moved to the end of the list and the other sources are re-indexed.

## -returns

The <b>MsiSourceListAddSourceEx</b> function  returns the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The user does not have the ability to add or move a source. Does not indicate whether the product or patch was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_CONFIGURATION</b></dt>
</dl>
</td>
<td width="60%">
The configuration data is corrupt.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_SERVICE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
Could not access the Windows Installer service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The source was inserted or updated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PRODUCT</b></dt>
</dl>
</td>
<td width="60%">
The specified product is unknown.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PATCH</b></dt>
</dl>
</td>
<td width="60%">
The specified patch is unknown.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FUNCTION_FAILED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected internal failure.

</td>
</tr>
</table>

## -remarks

Administrators can modify the installation  of   a product or patch   instance that exists  under the machine context or under their own per-user context (managed or unmanaged.) They can modify the installation of  a product or patch instance that exists under any user's per-user-managed context.  Administrators cannot modify another user's installation of a product or patch instance  that exists  under that other user's per-user-unmanaged context. 

Non-administrators cannot  modify the installation of  a product or patch instance that exists under another user's per-user context (managed or unmanaged.) They can modify the installation of  a product or patch instance that exists under their own per-user-unmanaged context.  They can modify the installation of a product or patch instance under the machine context or their own per-user-managed context only if they are enabled to browse for a product or patch source. Users can be enabled to browse for sources by setting policy. For more information, see the <a href="/windows/desktop/Msi/disablebrowse">DisableBrowse</a>, <a href="/windows/desktop/Msi/allowlockdownbrowse">AllowLockdownBrowse</a>, and <a href="/windows/desktop/Msi/alwaysinstallelevated">AlwaysInstallElevated</a> policies.





> [!NOTE]
> The msi.h header defines MsiSourceListAddSourceEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/allowlockdownbrowse">AllowLockdownBrowse</a>



<a href="/windows/desktop/Msi/alwaysinstallelevated">AlwaysInstallElevated</a>



<a href="/windows/desktop/Msi/disablebrowse">DisableBrowse</a>



<a href="/windows/desktop/api/msi/nf-msi-msisourcelistsetinfoa">MsiSourceListSetInfo</a>



<a href="/windows/desktop/Msi/not-supported-in-windows-installer-version-2-0">Not Supported in Windows Installer 2.0 and earlier</a>



<a href="/windows/desktop/Msi/productcode">ProductCode</a>



<a href="/windows/desktop/Msi/source-resiliency">Source Resiliency</a>
