---
UID: NF:msi.MsiSourceListEnumSourcesW
title: MsiSourceListEnumSourcesW function (msi.h)
description: The MsiSourceListEnumSources function enumerates the sources in the source list of a specified patch or product. (Unicode)
helpviewer_keywords: ["MSICODE_PATCH", "MSICODE_PRODUCT", "MSIINSTALLCONTEXT_MACHINE", "MSIINSTALLCONTEXT_USERMANAGED", "MSIINSTALLCONTEXT_USERUNMANAGED", "MSISOURCETYPE_NETWORK", "MSISOURCETYPE_URL", "MsiSourceListEnumSources", "MsiSourceListEnumSources function", "MsiSourceListEnumSourcesW", "NULL", "User SID", "msi/MsiSourceListEnumSources", "msi/MsiSourceListEnumSourcesW", "s-1-1-0", "setup.msisourcelistenumsources"]
old-location: setup\msisourcelistenumsources.htm
tech.root: setup
ms.assetid: 30a5efae-ebb5-4ff3-880a-4eed1bc8eed4
ms.date: 12/05/2018
ms.keywords: MSICODE_PATCH, MSICODE_PRODUCT, MSIINSTALLCONTEXT_MACHINE, MSIINSTALLCONTEXT_USERMANAGED, MSIINSTALLCONTEXT_USERUNMANAGED, MSISOURCETYPE_NETWORK, MSISOURCETYPE_URL, MsiSourceListEnumSources, MsiSourceListEnumSources function, MsiSourceListEnumSourcesA, MsiSourceListEnumSourcesW, NULL, User SID, msi/MsiSourceListEnumSources, msi/MsiSourceListEnumSourcesA, msi/MsiSourceListEnumSourcesW, s-1-1-0, setup.msisourcelistenumsources
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer 3.0 or later on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiSourceListEnumSourcesW (Unicode) and MsiSourceListEnumSourcesA (ANSI)
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
 - MsiSourceListEnumSourcesW
 - msi/MsiSourceListEnumSourcesW
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
 - MsiSourceListEnumSources
 - MsiSourceListEnumSourcesA
 - MsiSourceListEnumSourcesW
---

# MsiSourceListEnumSourcesW function


## -description

The <b>MsiSourceListEnumSources</b> function enumerates the sources in the source list of a specified patch or product.

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
A <b>NULL</b> indicates the current user who is logged on. When referencing the current user account, <i>szUserSID</i> can be <b>NULL</b> and <i>dwContext</i> can be  MSIINSTALLCONTEXT_USERMANAGED or MSIINSTALLCONTEXT_USERUNMANAGED.

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

The context of the product or patch instance. This parameter can contain one of the following values.

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

The <i>dwOptions</i> value determines the interpretation of the <i>szProductCodeOrPatchCode</i> value and the type of sources to clear. This parameter must be a combination of one of the following MSISOURCETYPE_* constants and one of the following MSICODE_* constants.

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

### -param dwIndex [in]

The index of the source to retrieve. This parameter must be 0 (zero) for the first call to the <b>MsiSourceListEnumSources</b> function, and then incremented for subsequent calls until the function returns ERROR_NO_MORE_ITEMS.  The index should be incremented only if the previous call returned ERROR_SUCCESS.

### -param szSource [in, optional]

A pointer to a  buffer that receives the path to the source that is  being enumerated. This buffer should be large enough to contain the received value. If the buffer is too small, the function returns ERROR_MORE_DATA and sets *<i>pcchSource</i> to the number of <b>TCHAR</b> in the value, not including the terminating NULL character.



If <i>szSource</i> is set to <b>NULL</b> and <i>pcchSource</i> is set to a valid pointer,  the function returns ERROR_SUCCESS and sets *<i>pcchSource</i> to the number of <b>TCHAR</b> in the value, not including the terminating NULL character.  The function can then be called again to retrieve the value, with <i>szSource</i> buffer large enough to contain *<i>pcchSource</i> + 1 characters. 

If <i>szSource</i> and <i>pcchSource</i> are both set to <b>NULL</b>, the function returns ERROR_SUCCESS if the value exists, without  retrieving the value.

### -param pcchSource [in, out, optional]

A pointer to a variable that specifies the number of <b>TCHAR</b> in the <i>szSource</i> buffer. When the function returns, this parameter is set to the size of the requested value whether or not the function copies the value into the specified buffer. The size is returned as the number of <b>TCHAR</b> in the requested value, not including the terminating null character.

This parameter can be set to <b>NULL</b> only if <i>szSource</i> is also <b>NULL</b>, otherwise the function returns ERROR_INVALID_PARAMETER.

## -returns

The <b>MsiSourceListEnumSources</b> function returns the following values.

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
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no more sources in the specified list to enumerate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
A source is enumerated successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PATCH</b></dt>
</dl>
</td>
<td width="60%">
The patch specified is not installed on the computer in the specified contexts.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PRODUCT</b></dt>
</dl>
</td>
<td width="60%">
The product specified is not installed on the computer in the specified contexts.

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

When making multiple calls to <b>MsiSourceListEnumSources</b> to enumerate all sources for a single product instance, each call must be made from the same thread.

An administrator can enumerate per-user unmanaged and managed installations for themselves, 		
		per-machine installations, and per-user managed installations for any user. An administrator cannot 			
		enumerate per-user unmanaged installations for other users. Non-administrators can only enumerate 		
		their own per-user unmanaged and managed installations and per-machine installations.





> [!NOTE]
> The msi.h header defines MsiSourceListEnumSources as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/installation-context">Installation Context</a>



<a href="/windows/desktop/Msi/not-supported-in-windows-installer-version-2-0">Not Supported in Windows Installer 2.0 and earlier</a>



<a href="/windows/desktop/Msi/productcode">ProductCode</a>
