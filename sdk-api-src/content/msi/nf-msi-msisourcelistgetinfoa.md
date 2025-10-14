---
UID: NF:msi.MsiSourceListGetInfoA
title: MsiSourceListGetInfoA function (msi.h)
description: The MsiSourceListGetInfo function retrieves information about the source list for a product or patch in a specific context. (ANSI)
helpviewer_keywords: ["INSTALLPROPERTY_DISKPROMPT", "INSTALLPROPERTY_LASTUSEDSOURCE", "INSTALLPROPERTY_LASTUSEDTYPE", "INSTALLPROPERTY_MEDIAPACKAGEPATH", "INSTALLPROPERTY_PACKAGENAME", "MSICODE_PATCH", "MSICODE_PRODUCT", "MSIINSTALLCONTEXT_MACHINE", "MSIINSTALLCONTEXT_USERMANAGED", "MSIINSTALLCONTEXT_USERUNMANAGED", "MsiSourceListGetInfoA", "NULL", "User SID", "msi/MsiSourceListGetInfoA"]
old-location: setup\msisourcelistgetinfo.htm
tech.root: setup
ms.assetid: 24188c7f-d9b5-4907-861a-9555c34cbd2d
ms.date: 12/05/2018
ms.keywords: INSTALLPROPERTY_DISKPROMPT, INSTALLPROPERTY_LASTUSEDSOURCE, INSTALLPROPERTY_LASTUSEDTYPE, INSTALLPROPERTY_MEDIAPACKAGEPATH, INSTALLPROPERTY_PACKAGENAME, MSICODE_PATCH, MSICODE_PRODUCT, MSIINSTALLCONTEXT_MACHINE, MSIINSTALLCONTEXT_USERMANAGED, MSIINSTALLCONTEXT_USERUNMANAGED, MsiSourceListGetInfo, MsiSourceListGetInfo function, MsiSourceListGetInfoA, MsiSourceListGetInfoW, NULL, User SID, msi/MsiSourceListGetInfo, msi/MsiSourceListGetInfoA, msi/MsiSourceListGetInfoW, setup.msisourcelistgetinfo
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer 3.0 or later on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiSourceListGetInfoW (Unicode) and MsiSourceListGetInfoA (ANSI)
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
 - MsiSourceListGetInfoA
 - msi/MsiSourceListGetInfoA
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
 - MsiSourceListGetInfo
 - MsiSourceListGetInfoA
 - MsiSourceListGetInfoW
---

# MsiSourceListGetInfoA function


## -description

The <b>MsiSourceListGetInfo</b> function retrieves information about the source list for a product or patch in a specific context.

## -parameters

### -param szProductCodeOrPatchCode [in]

The <a href="/windows/desktop/Msi/productcode">ProductCode</a> or patch GUID of the product or patch. Use a null-terminated string. If the string is longer than 39 characters, the function fails and returns ERROR_INVALID_PARAMETER. This parameter cannot be <b>NULL</b>.

### -param szUserSid [in, optional]

 This parameter can be a string security identifier (SID) that specifies the user account that contains the product or patch.  The SID is not validated or resolved. An incorrect SID can return ERROR_UNKNOWN_PRODUCT or ERROR_UNKNOWN_PATCH. When referencing a machine context, <i>szUserSID</i> must be <b>NULL</b> and <i>dwContext</i> must be MSIINSTALLCONTEXT_MACHINE.

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
<b>NULL</b> denotes the currently logged on user. When referencing the current user account, <i>szUserSID</i> can be <b>NULL</b> and <i>dwContext</i> can be  MSIINSTALLCONTEXT_USERMANAGED or MSIINSTALLCONTEXT_USERUNMANAGED.

</td>
</tr>
<tr>
<td width="40%"><a id="User_SID"></a><a id="user_sid"></a><a id="USER_SID"></a><dl>
<dt><b>User SID</b></dt>
</dl>
</td>
<td width="60%">
Specifies enumeration for a specific user in the system.  An example of a user SID is "S-1-3-64-2415071341-1358098788-3127455600-2561".

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  The special SID string s-1-5-18 (system) cannot be used to enumerate products or patches installed as per-machine.  Setting the SID value to s-1-5-18 returns ERROR_INVALID_PARAMETER.</div>
<div> </div>
<div class="alert"><b>Note</b>  The special SID string s-1-1-0 (everyone) should not be used. Setting the SID value to s-1-1-0 fails and returns ERROR_INVALID_PARAM.</div>
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

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
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

A null-terminated string that specifies the property value to retrieve. The <i>szProperty</i> parameter can be one of the following values.

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
The prompt template that is used when prompting the user for installation media.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_LASTUSEDSOURCE"></a><a id="installproperty_lastusedsource"></a><dl>
<dt><b>INSTALLPROPERTY_LASTUSEDSOURCE</b></dt>
<dt>"LastUsedSource"</dt>
</dl>
</td>
<td width="60%">
The most recently used source location for the product.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_LASTUSEDTYPE"></a><a id="installproperty_lastusedtype"></a><dl>
<dt><b>INSTALLPROPERTY_LASTUSEDTYPE</b></dt>
<dt>"LastUsedType"</dt>
</dl>
</td>
<td width="60%">
An "n" if the last-used source is a network location. A "u" if the last used source is a URL location. An "m" if the last used source is media. An empty string ("") if there is no last used source.  

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

### -param szValue [out, optional]

An output buffer that receives  the information. This buffer should be large enough to contain the information. If the buffer is too small, the function returns ERROR_MORE_DATA and sets *<i>pcchValue</i> to the number of <b>TCHAR</b> in the value, not including the terminating NULL character.



If the <i>szValue</i> is set to <b>NULL</b> and <i>pcchValue</i> is set to a valid pointer,  the function returns ERROR_SUCCESS and sets *<i>pcchValue</i> to the number of <b>TCHAR</b> in the value, not including the terminating NULL character.  The function can then be called again to retrieve the value, with <i>szValue</i> buffer large enough to contain *<i>pcchValue</i> + 1 characters. 

If <i>szValue</i> and <i>pcchValue</i> are both set to <b>NULL</b>, the function returns ERROR_SUCCESS if the value exists, without  retrieving the value.

### -param pcchValue [in, out, optional]

A pointer to a variable that specifies the number of <b>TCHAR</b> in the <i>szValue</i> buffer. When the function returns, this parameter is set to the size of the requested value whether or not the function copies the value into the specified buffer. The size is returned as the number of <b>TCHAR</b> in the requested value, not including the terminating null character.

This parameter can be set to <b>NULL</b> only if <i>szValue</i> is also <b>NULL</b>, otherwise the function returns ERROR_INVALID_PARAMETER.

## -returns

The <b>MsiSourceListGetInfo</b> function returns the following values.
					

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
The user does not have the ability to read the specified source list. This does not indicate whether a product or patch is found.

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
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The provided buffer is not sufficient to contain the requested data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The property is retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PATCH</b></dt>
</dl>
</td>
<td width="60%">
The patch is not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PRODUCT</b></dt>
</dl>
</td>
<td width="60%">
The product is not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The source property is not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FUNCTION_FAILED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected internal failure.

</td>
</tr>
</table>

## -remarks

Administrators can modify the installation  of   a product or patch   instance that exists  under the machine context or under their own per-user context (managed or unmanaged.) They can modify the installation of  a product or patch instance that exists under any user's per-user-managed context.  Administrators cannot modify another user's installation of a product or patch instance  that exists  under that other user's per-user-unmanaged context.

Non-administrators cannot  modify the installation of  a product or patch instance that exists under another user's per-user context (managed or unmanaged.) They can modify the installation of  a product or patch instance that exists under their own per-user-unmanaged context.  They can modify the installation of a product or patch instance under the machine context or their own per-user-managed context only if they are enabled to browse for a product or patch source. Users can be enabled to browse for sources by setting policy. For more information, see <a href="/windows/desktop/Msi/disablebrowse">DisableBrowse</a>, <a href="/windows/desktop/Msi/allowlockdownbrowse">AllowLockdownBrowse</a>, and <a href="/windows/desktop/Msi/alwaysinstallelevated">AlwaysInstallElevated</a> policies.





> [!NOTE]
> The msi.h header defines MsiSourceListGetInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/msi/nf-msi-msisourcelistsetinfoa">MsiSourceListSetInfo</a>



<a href="/windows/desktop/Msi/not-supported-in-windows-installer-version-2-0">Not Supported in Windows Installer 2.0 and earlier</a>



<a href="/windows/desktop/Msi/productcode">ProductCode</a>
