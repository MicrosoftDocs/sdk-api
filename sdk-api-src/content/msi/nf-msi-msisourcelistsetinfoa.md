---
UID: NF:msi.MsiSourceListSetInfoA
title: MsiSourceListSetInfoA function (msi.h)
description: Sets information about the source list for a product or patch in a specific context. (ANSI)
helpviewer_keywords: ["INSTALLPROPERTY_DISKPROMPT", "INSTALLPROPERTY_LASTUSEDSOURCE", "INSTALLPROPERTY_MEDIAPACKAGEPATH", "INSTALLPROPERTY_PACKAGENAME", "MSICODE_PATCH", "MSICODE_PRODUCT", "MSIINSTALLCONTEXT_MACHINE", "MSIINSTALLCONTEXT_USERMANAGED", "MSIINSTALLCONTEXT_USERUNMANAGED", "MSISOURCETYPE_NETWORK", "MSISOURCETYPE_URL", "MsiSourceListSetInfoA", "NULL", "User SID", "msi/MsiSourceListSetInfoA"]
old-location: setup\msisourcelistsetinfo.htm
tech.root: setup
ms.assetid: c449bb2e-2ced-4cde-9111-d3c10db669e1
ms.date: 12/05/2018
ms.keywords: INSTALLPROPERTY_DISKPROMPT, INSTALLPROPERTY_LASTUSEDSOURCE, INSTALLPROPERTY_MEDIAPACKAGEPATH, INSTALLPROPERTY_PACKAGENAME, MSICODE_PATCH, MSICODE_PRODUCT, MSIINSTALLCONTEXT_MACHINE, MSIINSTALLCONTEXT_USERMANAGED, MSIINSTALLCONTEXT_USERUNMANAGED, MSISOURCETYPE_NETWORK, MSISOURCETYPE_URL, MsiSourceListSetInfo, MsiSourceListSetInfo function, MsiSourceListSetInfoA, MsiSourceListSetInfoW, NULL, User SID, msi/MsiSourceListSetInfo, msi/MsiSourceListSetInfoA, msi/MsiSourceListSetInfoW, setup.msisourcelistsetinfo
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiSourceListSetInfoW (Unicode) and MsiSourceListSetInfoA (ANSI)
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
 - MsiSourceListSetInfoA
 - msi/MsiSourceListSetInfoA
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
 - MsiSourceListSetInfo
 - MsiSourceListSetInfoA
 - MsiSourceListSetInfoW
---

# MsiSourceListSetInfoA function


## -description

The <b>MsiSourceListSetInfo</b> function sets information about the source list for a product or patch in a specific context.

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
<b>NULL</b> denotes the currently logged on user. When referencing the current user account, <i>szUserSID</i> can be <b>NULL</b> and <i>dwContext</i> can be  <b>MSIINSTALLCONTEXT_USERMANAGED</b> or <b>MSIINSTALLCONTEXT_USERUNMANAGED</b>.

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
 

<div class="alert"><b>Note</b>  The special SID string "S-1-5-18" (system) cannot be used to enumerate products or patches installed as per-machine.  Setting the SID value to "S-1-5-18" returns "ERROR_INVALID_PARAMETER".</div>
<div> </div>
<div class="alert"><b>Note</b>  The special SID string "S-1-1-0" (everyone) should not be used. Setting the SID value to "S-1-1-0" fails and returns <b>ERROR_INVALID_PARAM</b>.</div>
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

The <i>dwOptions</i> value specifies the meaning of <i>szProductCodeOrPatchCode</i>.

If the property being set is "LastUsedSource", this parameter also specifies the type of source as network or URL. In this case, the <i>dwOptions</i> parameter must be a combination of one of the following <b>MSISOURCETYPE_*</b> constants and one of the following <b>MSICODE_*</b> constants.

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
<i>szProductCodeOrPatchCode</i> is a product code GUID.

</td>
</tr>
<tr>
<td width="40%"><a id="MSICODE_PATCH"></a><a id="msicode_patch"></a><dl>
<dt><b>MSICODE_PATCH</b></dt>
</dl>
</td>
<td width="60%">
<i>szProductCodeOrPatchCode</i> is a patch code GUID.

</td>
</tr>
</table>

### -param szProperty [in]

The parameter <i>szProperty</i> indicates the property value to set. Not all properties that can be retrieved through <a href="/windows/desktop/api/msi/nf-msi-msisourcelistgetinfoa">MsiSourceListGetInfo</a> can be set via a call to <b>MsiSourceListSetInfo</b>. The <i>szProperty</i> value can be one of the following values.

<table>
<tr>
<th>Name</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_MEDIAPACKAGEPATH"></a><a id="installproperty_mediapackagepath"></a><dl>
<dt><b>INSTALLPROPERTY_MEDIAPACKAGEPATH</b></dt>
<dt>"MediaPackagePath"</dt>
</dl>
</td>
<td width="60%">
The path relative to the root of the installation media.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_DISKPROMPT"></a><a id="installproperty_diskprompt"></a><dl>
<dt><b>INSTALLPROPERTY_DISKPROMPT</b></dt>
<dt>"DiskPrompt"</dt>
</dl>
</td>
<td width="60%">
The prompt template used when prompting the user for installation media.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_LASTUSEDSOURCE"></a><a id="installproperty_lastusedsource"></a><dl>
<dt><b>INSTALLPROPERTY_LASTUSEDSOURCE</b></dt>
<dt>"LastUsedSource"</dt>
</dl>
</td>
<td width="60%">
The most recently used source location for the product. If the source is not registered, the function calls <a href="/windows/desktop/api/msi/nf-msi-msisourcelistaddsourceexa">MsiSourceListAddSourceEx</a> to register it.  On successful registration, the function sets the source as the LastUsedSource.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_PACKAGENAME"></a><a id="installproperty_packagename"></a><dl>
<dt><b>INSTALLPROPERTY_PACKAGENAME</b></dt>
<dt>"PackageName"</dt>
</dl>
</td>
<td width="60%">
The name of the Windows Installer package or patch package on the source.

</td>
</tr>
</table>

### -param szValue [in]

The new value of the property. No validation of the new value is performed. This value cannot be <b>NULL</b>. It can be an empty string.

## -returns

The <b>MsiSourceListSetInfo</b> function returns the following values.

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
The user does not have the ability to set the source list for the specified product.

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
The Windows Installer service could not be accessed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The property was set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PATCH</b></dt>
</dl>
</td>
<td width="60%">
The patch was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PRODUCT</b></dt>
</dl>
</td>
<td width="60%">
The product was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The source property was not found.

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

An exception to the above rule is setting "LastUsedSource" to one of the registered sources. If the source is already registered, a non-administrator can set "LastUsedSource" to their own installations (managed or non-managed) and per-machine installations, irrespective of policies. 





> [!NOTE]
> The msi.h header defines MsiSourceListSetInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/installation-context">Installation Context</a>



<a href="/windows/desktop/api/msi/nf-msi-msisourcelistgetinfoa">MsiSourceListGetInfo</a>



<a href="/windows/desktop/Msi/not-supported-in-windows-installer-version-2-0">Not Supported in Windows Installer 2.0 and earlier</a>



<a href="/windows/desktop/Msi/productcode">ProductCode</a>
