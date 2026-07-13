---
UID: NF:msi.MsiEnumPatchesExA
title: MsiEnumPatchesExA function (msi.h)
description: Enumerates all patches in a specific context or across all contexts. (ANSI)
helpviewer_keywords: ["MSIINSTALLCONTEXT_MACHINE", "MSIINSTALLCONTEXT_USERMANAGED", "MSIINSTALLCONTEXT_USERUNMANAGED", "MSIPATCHSTATE_ALL", "MSIPATCHSTATE_APPLIED", "MSIPATCHSTATE_OBSOLETED", "MSIPATCHSTATE_REGISTERED", "MSIPATCHSTATE_SUPERSEDED", "MsiEnumPatchesExA", "NULL", "User SID", "msi/MsiEnumPatchesExA", "s-1-1-0"]
old-location: setup\msienumpatchesex.htm
tech.root: setup
ms.assetid: 32edcc56-190a-465f-b341-56dc60ab0589
ms.date: 12/05/2018
ms.keywords: MSIINSTALLCONTEXT_MACHINE, MSIINSTALLCONTEXT_USERMANAGED, MSIINSTALLCONTEXT_USERUNMANAGED, MSIPATCHSTATE_ALL, MSIPATCHSTATE_APPLIED, MSIPATCHSTATE_OBSOLETED, MSIPATCHSTATE_REGISTERED, MSIPATCHSTATE_SUPERSEDED, MsiEnumPatchesEx, MsiEnumPatchesEx function, MsiEnumPatchesExA, MsiEnumPatchesExW, NULL, User SID, msi/MsiEnumPatchesEx, msi/MsiEnumPatchesExA, msi/MsiEnumPatchesExW, s-1-1-0, setup.msienumpatchesex
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiEnumPatchesExW (Unicode) and MsiEnumPatchesExA (ANSI)
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
 - MsiEnumPatchesExA
 - msi/MsiEnumPatchesExA
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
 - MsiEnumPatchesEx
 - MsiEnumPatchesExA
 - MsiEnumPatchesExW
---

# MsiEnumPatchesExA function


## -description

The <b>MsiEnumPatchesEx</b> function enumerates all patches in a specific context or across all contexts. Patches already applied to products are enumerated. Patches that have been registered but not yet applied to products are also enumerated.

## -parameters

### -param szProductCode [in, optional]

A null-terminated string that specifies the <a href="/windows/desktop/Msi/productcode">ProductCode</a> GUID of the product whose patches are enumerated. If non-<b>NULL</b>, patch enumeration is restricted to instances of this product under the user and context specified by <i>szUserSid</i> and <i>dwContext</i>. If <b>NULL</b>, the patches for all products under the specified context are enumerated.

### -param szUserSid [in, optional]

A null-terminated string that specifies a security identifier (SID) that restricts the context of enumeration. The special SID string "S-1-1-0" (Everyone) specifies enumeration across all users in the system. A SID value other than "S-1-1-0" is considered a user SID and restricts enumeration to that user.  When enumerating for a user other than current user, any patches that were applied in a per-user-unmanaged context using a version less than Windows Installer version 3.0, are not enumerated. This parameter can be set to <b>NULL</b> to specify the current user.

<table>
<tr>
<th>SID type</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NULL"></a><a id="null"></a><dl>
<dt><b>NULL</b></dt>
</dl>
</td>
<td width="60%">
Specifies the currently logged-on user.

</td>
</tr>
<tr>
<td width="40%"><a id="User_SID"></a><a id="user_sid"></a><a id="USER_SID"></a><dl>
<dt><b>User SID</b></dt>
</dl>
</td>
<td width="60%">
An enumeration for a specific user in the system.  An example of user SID is "S-1-3-64-2415071341-1358098788-3127455600-2561".

</td>
</tr>
<tr>
<td width="40%"><a id="s-1-1-0"></a><a id="S-1-1-0"></a><dl>
<dt><b>s-1-1-0</b></dt>
</dl>
</td>
<td width="60%">
An enumeration across all users in the system.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  The special SID string "S-1-5-18" (System) cannot be used to enumerate products or patches installed as per-machine.  Setting the SID value to "S-1-5-18" returns <b>ERROR_INVALID_PARAMETER</b>. When <i>dwContext</i> is set to <b>MSIINSTALLCONTEXT_MACHINE</b> only, <i>szUserSid</i> must be <b>NULL</b>.</div>
<div> </div>

### -param dwContext [in]

Restricts the  enumeration to one or a combination of contexts. This parameter can be any one or a combination of the  following values.

<table>
<tr>
<th>Context</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERMANAGED"></a><a id="msiinstallcontext_usermanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERMANAGED</b></dt>
</dl>
</td>
<td width="60%">
The enumeration that is extended to all per-user-managed installations for the users that <i>szUserSid</i> specifies. An invalid SID returns no items.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERUNMANAGED"></a><a id="msiinstallcontext_userunmanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERUNMANAGED</b></dt>
</dl>
</td>
<td width="60%">
In this context, only patches installed with Windows Installer version 3.0 are enumerated for users that are not the current user.  For the current user, the function enumerates all installed and new  patches. An invalid SID for <i>szUserSid</i> returns no items.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_MACHINE"></a><a id="msiinstallcontext_machine"></a><dl>
<dt><b>MSIINSTALLCONTEXT_MACHINE</b></dt>
</dl>
</td>
<td width="60%">
An enumeration that is  extended to all per-machine installations. When <i>dwContext</i> is set to <b>MSIINSTALLCONTEXT_MACHINE</b> only, the <i>szUserSid</i> parameter must be <b>NULL</b>.

</td>
</tr>
</table>

### -param dwFilter [in]

The filter for enumeration. This parameter can be one or a combination of the following parameters.

<table>
<tr>
<th>Filter</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSIPATCHSTATE_APPLIED"></a><a id="msipatchstate_applied"></a><dl>
<dt><b>MSIPATCHSTATE_APPLIED</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The enumeration includes patches that have been applied. Enumeration does not include superseded or obsolete patches.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIPATCHSTATE_SUPERSEDED"></a><a id="msipatchstate_superseded"></a><dl>
<dt><b>MSIPATCHSTATE_SUPERSEDED</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The enumeration includes patches that are marked as superseded.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIPATCHSTATE_OBSOLETED"></a><a id="msipatchstate_obsoleted"></a><dl>
<dt><b>MSIPATCHSTATE_OBSOLETED</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The enumeration includes patches that are marked as obsolete.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIPATCHSTATE_REGISTERED"></a><a id="msipatchstate_registered"></a><dl>
<dt><b>MSIPATCHSTATE_REGISTERED</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
The enumeration includes patches that are registered but not yet applied. The <a href="/windows/desktop/api/msi/nf-msi-msisourcelistaddsourceexa">MsiSourceListAddSourceEx</a> function can register new patches.

<div class="alert"><b>Note</b>  Patches registered for users other than current user and applied in the per-user-unmanaged context are not enumerated.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="MSIPATCHSTATE_ALL"></a><a id="msipatchstate_all"></a><dl>
<dt><b>MSIPATCHSTATE_ALL</b></dt>
<dt>15</dt>
</dl>
</td>
<td width="60%">
The enumeration includes all applied, obsolete, superseded, and registered patches.

</td>
</tr>
</table>

### -param dwIndex [in]

The index of the patch to retrieve. This parameter must be zero for the first call to the <b>MsiEnumPatchesEx</b> function and then incremented for subsequent calls. The <i>dwIndex</i> parameter should be incremented only if the previous call returned ERROR_SUCCESS.

### -param szPatchCode [out, optional]

An output buffer to contain the GUID of the patch being enumerated. The buffer should be large enough to hold the GUID. This parameter can be <b>NULL</b>.

### -param szTargetProductCode [out, optional]

An output buffer to contain the <a href="/windows/desktop/Msi/productcode">ProductCode</a> GUID of the product that receives this patch. The buffer should be large enough to hold the GUID. This parameter can be <b>NULL</b>.

### -param pdwTargetProductContext [out, optional]

Returns the context of the patch being enumerated. The output value can be  <b>MSIINSTALLCONTEXT_USERMANAGED</b>,  <b>MSIINSTALLCONTEXT_USERUNMANAGED</b>, or <b>MSIINSTALLCONTEXT_MACHINE</b>. This parameter can be <b>NULL</b>.

### -param szTargetUserSid [out, optional]

An output buffer that receives  the string SID of the account under which this patch instance exists. This buffer returns an empty string for a per-machine context.

This buffer should be large enough to contain the SID. If the buffer is too small, the function returns <b>ERROR_MORE_DATA</b> and sets *<i>pcchTargetUserSid</i> to the number of <b>TCHAR</b> in the value, not including the terminating NULL character.

If the <i>szTargetUserSid</i> is set to <b>NULL</b> and <i>pcchTargetUserSid</i> is set to a valid pointer,  the function returns <b>ERROR_SUCCESS</b> and sets *<i>pcchTargetUserSid</i> to the number of <b>TCHAR</b> in the value, not including the terminating <b>NULL</b> character.  The function can then be called again to retrieve the value, with <i>szTargetUserSid</i> buffer large enough to contain *<i>pcchTargetUserSid</i> + 1 characters.

If <i>szTargetUserSid</i> and <i>pcchTargetUserSid</i> are both set to <b>NULL</b>, the function returns <b>ERROR_SUCCESS</b> if the value exists, without  retrieving the value.

### -param pcchTargetUserSid [in, out, optional]

A pointer to a variable that specifies the number of <b>TCHAR</b> in the <i>szTargetUserSid</i> buffer. When the function returns, this parameter is set to the size of the requested value whether or not the function copies the value into the specified buffer. The size is returned as the number of <b>TCHAR</b> in the requested value, not including the terminating null character.

This parameter can be set to <b>NULL</b> only if <i>szTargetUserSid</i> is also <b>NULL</b>, otherwise the function returns ERROR_INVALID_PARAMETER.

## -returns

The <b>MsiEnumPatchesEx</b> function returns one of the following values.

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
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no more patches to enumerate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The patch is successfully enumerated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PRODUCT</b></dt>
</dl>
</td>
<td width="60%">
The product that  <i>szProduct</i> specifies is not installed on the computer in the specified contexts.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
This is returned when <i>pcchTargetUserSid</i> points to a buffer size less than required to copy the SID. In this case, the user can fix the buffer and call <a href="/windows/desktop/api/msi/nf-msi-msienumpatchesexa">MsiEnumPatchesEx</a>  again for the same index value.

</td>
</tr>
</table>

## -remarks

Non-administrators can  enumerate patches within  their visibility only. Administrators can enumerate patches for other user contexts.





> [!NOTE]
> The msi.h header defines MsiEnumPatchesEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/installation-context">Installation Context</a>



<a href="/windows/desktop/api/msi/nf-msi-msisourcelistaddsourceexa">MsiSourceListAddSourceEx</a>



<a href="/windows/desktop/Msi/not-supported-in-windows-installer-version-2-0">Not Supported in Windows Installer 2.0 and earlier</a>



<a href="/windows/desktop/Msi/productcode">ProductCode</a>
