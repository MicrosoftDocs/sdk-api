---
UID: NF:msi.MsiSourceListEnumMediaDisksA
title: MsiSourceListEnumMediaDisksA function (msi.h)
description: The MsiSourceListEnumMediaDisks function enumerates the list of disks registered for the media source for a patch or product. (ANSI)
helpviewer_keywords: ["MSICODE_PATCH", "MSICODE_PRODUCT", "MSIINSTALLCONTEXT_MACHINE", "MSIINSTALLCONTEXT_USERMANAGED", "MSIINSTALLCONTEXT_USERUNMANAGED", "MsiSourceListEnumMediaDisksA", "NULL", "User SID", "msi/MsiSourceListEnumMediaDisksA", "s-1-1-0"]
old-location: setup\msisourcelistenummediadisks.htm
tech.root: setup
ms.assetid: 29bf12f4-f9e0-4853-8f03-a31a855b2ad6
ms.date: 12/05/2018
ms.keywords: MSICODE_PATCH, MSICODE_PRODUCT, MSIINSTALLCONTEXT_MACHINE, MSIINSTALLCONTEXT_USERMANAGED, MSIINSTALLCONTEXT_USERUNMANAGED, MsiSourceListEnumMediaDisks, MsiSourceListEnumMediaDisks function, MsiSourceListEnumMediaDisksA, MsiSourceListEnumMediaDisksW, NULL, User SID, msi/MsiSourceListEnumMediaDisks, msi/MsiSourceListEnumMediaDisksA, msi/MsiSourceListEnumMediaDisksW, s-1-1-0, setup.msisourcelistenummediadisks
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer 3.0 or later on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiSourceListEnumMediaDisksW (Unicode) and MsiSourceListEnumMediaDisksA (ANSI)
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
 - MsiSourceListEnumMediaDisksA
 - msi/MsiSourceListEnumMediaDisksA
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
 - MsiSourceListEnumMediaDisks
 - MsiSourceListEnumMediaDisksA
 - MsiSourceListEnumMediaDisksW
---

# MsiSourceListEnumMediaDisksA function


## -description

The <b>MsiSourceListEnumMediaDisks</b> function enumerates the list of disks registered for the media source for a patch or product.

## -parameters

### -param szProductCodeOrPatchCode [in]

The <a href="/windows/desktop/Msi/productcode">ProductCode</a> or patch GUID of the product or patch. Use a null-terminated string. If the string is longer than 39 characters, the function fails and returns ERROR_INVALID_PARAMETER. This parameter cannot be <b>NULL</b>.

### -param szUserSid [in, optional]

A string SID that specifies the user account that contains the product or patch.  The SID is not validated or resolved. An incorrect SID can return ERROR_UNKNOWN_PRODUCT or ERROR_UNKNOWN_PATCH. When referencing a machine context, <i>szUserSID</i> must be <b>NULL</b> and <i>dwContext</i> must be MSIINSTALLCONTEXT_MACHINE. 

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
A <b>NULL</b> denotes the currently logged on user. When referencing the current user account, <i>szUserSID</i> can be <b>NULL</b> and <i>dwContext</i> can be  MSIINSTALLCONTEXT_USERMANAGED or MSIINSTALLCONTEXT_USERUNMANAGED.

</td>
</tr>
<tr>
<td width="40%"><a id="User_SID"></a><a id="user_sid"></a><a id="USER_SID"></a><dl>
<dt><b>User SID</b></dt>
</dl>
</td>
<td width="60%">
An enumeration for a specific user in the system.  An example of a user SID is "S-1-3-64-2415071341-1358098788-3127455600-2561".

</td>
</tr>
<tr>
<td width="40%"><a id="s-1-1-0"></a><a id="S-1-1-0"></a><dl>
<dt><b>s-1-1-0</b></dt>
</dl>
</td>
<td width="60%">
The special SID string s-1-1-0 (everyone) specifies enumeration across all users in the system.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  The special SID string s-1-5-18 (system) cannot be used to enumerate products or patches installed as per-machine.  Setting the SID value to s-1-5-18 returns ERROR_INVALID_PARAMETER.</div>
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

The <i>dwOptions</i> value that  specifies the meaning of <i>szProductCodeOrPatchCode</i>.

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

### -param dwIndex [in]

The index of the source to retrieve. This parameter must be 0 (zero) for the first call to the <b>MsiSourceListEnumMediaDisks</b>  function, and then incremented for subsequent calls until the function returns ERROR_NO_MORE_ITEMS.

### -param pdwDiskId [out, optional]

On entry to <b>MsiSourceListEnumMediaDisks</b> this parameter provides a pointer to a <b>DWORD</b> to receive the ID of the disk that is being enumerated.   This parameter is optional.

### -param szVolumeLabel [out, optional]

An output buffer that receives  the volume label of the disk that is being enumerated. This buffer should be large enough to contain the information. If the buffer is too small, the function returns ERROR_MORE_DATA and sets *<i>pcchVolumeLabel</i> to the number of <b>TCHAR</b> in the value, not including the terminating NULL character.



If <i>szVolumeLabel</i> and <i>pcchVolumeLabel</i> are both set to <b>NULL</b>, the function returns ERROR_SUCCESS if the value exists, without  retrieving the value.

### -param pcchVolumeLabel [in, out, optional]

A pointer to a variable that specifies the number of <b>TCHAR</b> in the <i>szVolumeLabel</i> buffer. When the function returns, this parameter is the number of <b>TCHAR</b> in the received  value,  not including the terminating null character. 

This parameter can be set to <b>NULL</b> only if <i>szVolumeLabel</i> is also <b>NULL</b>, otherwise the function returns ERROR_INVALID_PARAMETER.

### -param szDiskPrompt [out, optional]

An output buffer that receives  the disk prompt of the disk that is being enumerated. This buffer should be large enough to contain the information. If the buffer is too small, the function returns ERROR_MORE_DATA and sets *<i>pcchDiskPrompt</i> to the number of <b>TCHAR</b> in the value, not including the terminating NULL character.



If the <i>szDiskPrompt</i> is set to <b>NULL</b> and <i>pcchDiskPrompt</i> is set to a valid pointer,  the function returns ERROR_SUCCESS and sets *<i>pcchDiskPrompt</i> to the number of <b>TCHAR</b> in the value, not including the terminating NULL character.  The function can then be called again to retrieve the value, with <i>szDiskPrompt</i> buffer large enough to contain *<i>pcchDiskPrompt</i> + 1 characters.

If <i>szDiskPrompt</i> and <i>pcchDiskPrompt</i> are both set to <b>NULL</b>, the function returns ERROR_SUCCESS if the value exists, without  retrieving the value.

### -param pcchDiskPrompt [in, out, optional]

A pointer to a variable that specifies the number of <b>TCHAR</b> in the <i>szDiskPrompt</i> buffer. When the function returns, this parameter is set to the size of the requested value whether or not the function copies the value into the specified buffer. The size is returned as the number of <b>TCHAR</b> in the requested value, not including the terminating null character.

This parameter can be set to <b>NULL</b> only if <i>szDiskPrompt</i> is also <b>NULL</b>, otherwise the function returns ERROR_INVALID_PARAMETER.

## -returns

The <b>MsiSourceListEnumMediaDisks</b> function returns the following values.

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
The user does not have the ability to read the specified media source or the specified product or patch. This does not indicate whether a media source, product, or patch is found.

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
There are no more disks registered for this product or patch.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The value is enumerated successfully.

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
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer that is provided is too small to contain the requested information.

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

When making multiple calls to <b>MsiSourceListEnumMediaDisks</b> to enumerate all the sources for a single product instance, each call must be made from the same thread.

An administrator can enumerate per-user unmanaged and managed installations for themselves, 		
		per-machine installations, and per-user managed installations for any user. An administrator cannot 			
		enumerate per-user unmanaged installations for other users. Non-administrators can only enumerate 		
		their own per-user unmanaged and managed installations and per-machine installations.





> [!NOTE]
> The msi.h header defines MsiSourceListEnumMediaDisks as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/installation-context">Installation Context</a>



<a href="/windows/desktop/Msi/not-supported-in-windows-installer-version-2-0">Not Supported in Windows Installer 2.0 and earlier</a>



<a href="/windows/desktop/Msi/productcode">ProductCode</a>
