---
UID: NF:msi.MsiGetPatchInfoExA
title: MsiGetPatchInfoExA function (msi.h)
description: Queries for information about the application of a patch to a specified instance of a product. (ANSI)
helpviewer_keywords: ["INSTALLPROPERTY_DISPLAYNAME", "INSTALLPROPERTY_INSTALLDATE", "INSTALLPROPERTY_LOCALPACKAGE", "INSTALLPROPERTY_MOREINFOURL", "INSTALLPROPERTY_PATCHSTATE", "INSTALLPROPERTY_TRANSFORMS", "INSTALLPROPERTY_UNINSTALLABLE", "MSIINSTALLCONTEXT_MACHINE", "MSIINSTALLCONTEXT_USERMANAGED", "MSIINSTALLCONTEXT_USERUNMANAGED", "MsiGetPatchInfoExA", "NULL", "User SID", "msi/MsiGetPatchInfoExA"]
old-location: setup\msigetpatchinfoex.htm
tech.root: setup
ms.assetid: 18acad03-7794-4c29-8cac-1dd3ea64369a
ms.date: 12/05/2018
ms.keywords: INSTALLPROPERTY_DISPLAYNAME, INSTALLPROPERTY_INSTALLDATE, INSTALLPROPERTY_LOCALPACKAGE, INSTALLPROPERTY_MOREINFOURL, INSTALLPROPERTY_PATCHSTATE, INSTALLPROPERTY_TRANSFORMS, INSTALLPROPERTY_UNINSTALLABLE, MSIINSTALLCONTEXT_MACHINE, MSIINSTALLCONTEXT_USERMANAGED, MSIINSTALLCONTEXT_USERUNMANAGED, MsiGetPatchInfoEx, MsiGetPatchInfoEx function, MsiGetPatchInfoExA, MsiGetPatchInfoExW, NULL, User SID, msi/MsiGetPatchInfoEx, msi/MsiGetPatchInfoExA, msi/MsiGetPatchInfoExW, setup.msigetpatchinfoex
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiGetPatchInfoExW (Unicode) and MsiGetPatchInfoExA (ANSI)
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
 - MsiGetPatchInfoExA
 - msi/MsiGetPatchInfoExA
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
 - MsiGetPatchInfoEx
 - MsiGetPatchInfoExA
 - MsiGetPatchInfoExW
---

# MsiGetPatchInfoExA function


## -description

The <b>MsiGetPatchInfoEx</b>  function queries for information about the application of a patch to a specified instance of a product.

## -parameters

### -param szPatchCode [in]

A null-terminated string that contains the GUID of the patch. This parameter cannot be <b>NULL</b>.

### -param szProductCode [in]

A null-terminated string that contains the <a href="/windows/desktop/Msi/productcode">ProductCode</a> GUID of the product instance. This parameter cannot be <b>NULL</b>.

### -param szUserSid [in]

A null-terminated string that specifies the security identifier (SID) under which the instance of the patch being queried exists.  Using a <b>NULL</b> value specifies the current user.

<table>
<tr>
<th>SID</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NULL"></a><a id="null"></a><dl>
<dt><b>NULL</b></dt>
</dl>
</td>
<td width="60%">
Specifies the user that is logged on.

</td>
</tr>
<tr>
<td width="40%"><a id="User_SID"></a><a id="user_sid"></a><a id="USER_SID"></a><dl>
<dt><b>User SID</b></dt>
</dl>
</td>
<td width="60%">
Specifies the enumeration for a specific user ID in the system.  The following example identifies a possible user SID: "S-1-3-64-2415071341-1358098788-3127455600-2561".

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  The special SID string "S-1-5-18" (system) cannot be used to enumerate products installed as per-machine. If <i>dwContext</i> is <b>MSIINSTALLCONTEXT_MACHINE</b>, <i>szUserSid</i> must be <b>NULL</b>.</div>
<div> </div>

### -param dwContext [in]

Restricts the  enumeration to a per-user-unmanaged,  per-user-managed, or per-machine context. This parameter can be any one of the  following values.

<table>
<tr>
<th>Context</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERMANAGED"></a><a id="msiinstallcontext_usermanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERMANAGED</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Query that is extended to all per–user-managed installations for the users that <i>szUserSid</i>  specifies.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERUNMANAGED"></a><a id="msiinstallcontext_userunmanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERUNMANAGED</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Query that is extended to all per–user-unmanaged installations for the users that  <i>szUserSid</i> specifies.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_MACHINE"></a><a id="msiinstallcontext_machine"></a><dl>
<dt><b>MSIINSTALLCONTEXT_MACHINE</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Query that is extended to all per-machine installations.

</td>
</tr>
</table>

### -param szProperty [in]

A null-terminated string that specifies the property value to retrieve. The <i>szProperty</i> parameter can be one of the following:

<table>
<tr>
<th>Name</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_LOCALPACKAGE"></a><a id="installproperty_localpackage"></a><dl>
<dt><b>INSTALLPROPERTY_LOCALPACKAGE</b></dt>
<dt>"LocalPackage"</dt>
</dl>
</td>
<td width="60%">
Gets the cached patch file that the product uses.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_TRANSFORMS"></a><a id="installproperty_transforms"></a><dl>
<dt><b>INSTALLPROPERTY_TRANSFORMS</b></dt>
<dt>"Transforms"</dt>
</dl>
</td>
<td width="60%">
Gets the set of patch transforms that the last patch installation applied to the product. This value may not be available for per-user, non-managed applications if the user is not logged on.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_INSTALLDATE"></a><a id="installproperty_installdate"></a><dl>
<dt><b>INSTALLPROPERTY_INSTALLDATE</b></dt>
<dt>"InstallDate"</dt>
</dl>
</td>
<td width="60%">
Gets the last time this product received service. The value of this property is replaced each time a patch is applied or removed from the product or the /v <a href="/windows/desktop/Msi/command-line-options">Command-Line Option</a> is used to repair the product.  If the product has received no repairs or patches this property contains the time this product was installed on this computer.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_UNINSTALLABLE"></a><a id="installproperty_uninstallable"></a><dl>
<dt><b>INSTALLPROPERTY_UNINSTALLABLE</b></dt>
<dt>"Uninstallable"</dt>
</dl>
</td>
<td width="60%">
Returns "1" if the patch is marked as possible to uninstall from the product.  In this case, the installer can still block the uninstallation if this patch is required by another patch that cannot be uninstalled.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_PATCHSTATE"></a><a id="installproperty_patchstate"></a><dl>
<dt><b>INSTALLPROPERTY_PATCHSTATE</b></dt>
<dt>"State"</dt>
</dl>
</td>
<td width="60%">
Returns "1" if this patch is currently applied to the product. Returns "2" if this patch is superseded by another patch. Returns  "4" if this patch is obsolete.   These values correspond to the constants the <i>dwFilter</i> parameter of <a href="/windows/desktop/api/msi/nf-msi-msienumpatchesexa">MsiEnumPatchesEx</a> uses.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_DISPLAYNAME"></a><a id="installproperty_displayname"></a><dl>
<dt><b>INSTALLPROPERTY_DISPLAYNAME</b></dt>
<dt>"DisplayName"</dt>
</dl>
</td>
<td width="60%">
Get the registered display name for the patch. For patches that do not
include the DisplayName property in the <a href="/windows/desktop/Msi/msipatchmetadata-table">MsiPatchMetadata</a> table, the
      returned display name is an empty string ("").

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_MOREINFOURL"></a><a id="installproperty_moreinfourl"></a><dl>
<dt><b>INSTALLPROPERTY_MOREINFOURL</b></dt>
<dt>"MoreInfoURL"</dt>
</dl>
</td>
<td width="60%">
Get the registered support information URL for the patch. For patches that do not include the MoreInfoURL property in the 
      <a href="/windows/desktop/Msi/msipatchmetadata-table">MsiPatchMetadata</a> table, the returned support information URL is an
      empty string ("").

</td>
</tr>
</table>

### -param lpValue [out, optional]

This parameter is a pointer to a  buffer that receives the property value. This buffer should be large enough to contain the information. If the buffer is too small, the function returns <b>ERROR_MORE_DATA</b> and sets *<i>pcchValue</i> to the number of <b>TCHAR</b> in the property value, not including the terminating <b>NULL</b> character.

If <i>lpValue</i> is set to <b>NULL</b> and <i>pcchValue</i> is set to a valid pointer,  the function returns <b>ERROR_SUCCESS</b> and sets *<i>pcchValue</i> to the number of <b>TCHAR</b> in the value, not including the terminating <b>NULL</b> character.  The function can then be called again to retrieve the value, with <i>lpValue</i> buffer large enough to contain *<i>pcchValue</i> + 1 characters.

If <i>lpValue</i> and <i>pcchValue</i> are both set to <b>NULL</b>, the function returns <b>ERROR_SUCCESS</b> if the value exists, without  retrieving the value.

### -param pcchValue [in, out]

When calling the function, this parameter should be a pointer to a variable that specifies the number of <b>TCHAR</b> in the <i>lpValue</i> buffer. When the function returns, this parameter is set to the size of the requested value whether or not the function copies the value into the specified buffer. The size is returned as the number of <b>TCHAR</b> in the requested value, not including the terminating null character.

This parameter can be set to <b>NULL</b> only if <i>lpValue</i> is also <b>NULL</b>. Otherwise, the function returns <b>ERROR_INVALID_PARAMETER</b>.

## -returns

The <b>MsiGetPatchInfoEx</b> function returns the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The function fails trying to access a resource with insufficient privileges.

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
<dt><b>ERROR_FUNCTION_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The function fails and the error is not identified in other error codes.

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
The value does not fit in the provided buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The patch is enumerated successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PRODUCT</b></dt>
</dl>
</td>
<td width="60%">
The product that <i>szProduct</i> specifies is not installed on the computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The property is unrecognized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PATCH</b></dt>
</dl>
</td>
<td width="60%">
The patch is unrecognized.

</td>
</tr>
</table>

## -remarks

<b>Windows Installer 2.0:  </b>Not supported. This function is available beginning with Windows Installer version 3.0.

A user may query patch data for any product instance that is visible. The administrator group can query patch data for any product instance and any user on the computer. Not all values are guaranteed to be available for per-user, non-managed applications if the user is not logged on.





> [!NOTE]
> The msi.h header defines MsiGetPatchInfoEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/productcode">ProductCode</a>



<a href="/windows/desktop/Msi/removing-patches">Removing Patches</a>
