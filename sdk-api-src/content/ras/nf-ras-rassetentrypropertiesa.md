---
UID: NF:ras.RasSetEntryPropertiesA
title: RasSetEntryPropertiesA function (ras.h)
description: The RasSetEntryProperties function changes the connection information for an entry in the phone book or creates a new phone-book entry. (ANSI)
helpviewer_keywords: ["RasSetEntryPropertiesA", "ras/RasSetEntryPropertiesA"]
old-location: rras\rassetentryproperties.htm
tech.root: RRAS
ms.assetid: 6532b48b-0d80-4993-800e-c808bb7540d6
ms.date: 12/05/2018
ms.keywords: RasSetEntryProperties, RasSetEntryProperties function [RAS], RasSetEntryPropertiesA, RasSetEntryPropertiesW, _ras_rassetentryproperties, ras/RasSetEntryProperties, ras/RasSetEntryPropertiesA, ras/RasSetEntryPropertiesW, rras.rassetentryproperties
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasSetEntryPropertiesW (Unicode) and RasSetEntryPropertiesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RasSetEntryPropertiesA
 - ras/RasSetEntryPropertiesA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasapi32.dll
api_name:
 - RasSetEntryProperties
 - RasSetEntryPropertiesA
 - RasSetEntryPropertiesW
---

# RasSetEntryPropertiesA function


## -description

The <b>RasSetEntryProperties</b> function changes the 
    connection information for an entry in the phone book or creates a new phone-book entry.

## -parameters

### -param unnamedParam1 [in]

Pointer to a null-terminated string that specifies the full path and file name of a phone-book (PBK) file. 
      If this parameter is <b>NULL</b>, the function uses the current default phone-book file. 
      The default phone-book file is the one selected by the user in the <b>User Preferences</b> 
      property sheet of the <b>Dial-Up Networking</b> dialog box.

### -param unnamedParam2 [in]

Pointer to a null-terminated string that specifies an entry name.

If the entry name matches an existing entry, 
       <b>RasSetEntryProperties</b> modifies the properties 
       of that entry.

If the entry name does not match an existing entry, 
       <b>RasSetEntryProperties</b> creates a new 
       phone-book entry. For new entries, call the 
       <a href="/windows/desktop/api/ras/nf-ras-rasvalidateentrynamea">RasValidateEntryName</a> function to validate the 
       entry name before calling 
       <b>RasSetEntryProperties</b>.

### -param unnamedParam3 [in]

Pointer to the <a href="/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)">RASENTRY</a> structure that specifies the 
       new connection data to be associated with the phone-book entry indicated by the 
       <i>lpszEntry</i> parameter.

The caller must provide values for the following members in the 
       <a href="/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)">RASENTRY</a> structure.

<ul>
<li><b>dwSize</b></li>
<li><b>szLocalPhoneNumber</b></li>
<li><b>szDeviceName</b></li>
<li><b>szDeviceType</b></li>
<li><b>dwFramingProtocol</b></li>
<li><b>dwfOptions</b></li>
<li><b>dwType</b></li>
</ul>
<b>Windows XP or later:  </b><b>dwType</b> is supported.

If values are not provided for these members, 
       <b>RasSetEntryProperties</b> fails with 
       <b>ERROR_INVALID_PARAMETER</b>.

The structure might be followed by an array of null-terminated alternate phone number strings. The last 
       string is terminated by two consecutive null characters. The <b>dwAlternateOffset</b> 
       member of the <a href="/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)">RASENTRY</a> structure contains the offset to 
       the first string.

### -param unnamedParam4 [in]

Specifies the size, in bytes, of the buffer identified by the <i>lpRasEntry</i> 
      parameter.

### -param unnamedParam5 [in]

Pointer to a buffer that specifies device-specific configuration information. This is opaque TAPI device 
      configuration information. For more information about TAPI device configuration, see the 
      <a href="/windows/desktop/api/tapi/nf-tapi-linegetdevconfig">lineGetDevConfig</a> function in 
      <a href="/windows/desktop/Tapi/telephony-application-programming-interfaces">Telephony Application Programming Interfaces (TAPI)</a> 
      in the Platform SDK.
      

<b>Windows XP:  </b>This parameter is unused. The calling function should set this parameter to 
        <b>NULL</b>.

### -param unnamedParam6 [in]

Specifies the size, in bytes, of the <i>lpbDeviceInfo</i> buffer.
      

<b>Windows XP:  </b>This parameter is unused. The calling function should set this parameter to zero.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from 
       <a href="/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> 
       or WinError.h.

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
The user does not have the correct privileges.  Only an administrator can complete this task.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUFFER_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The address or buffer specified by <i>lpRasEntry</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_OPEN_PHONEBOOK</b></dt>
</dl>
</td>
<td width="60%">
The phone book is corrupted or missing components.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)">RASENTRY</a> structure pointed to by the 
        <i>lpRasEntry</i> parameter does not contain adequate information, or the specified entry 
        does not exist in the phone book. See the description for <i>lpRasEntry</i> to see what 
        information is required.

</td>
</tr>
</table>

## -remarks

When setting properties for an all-users connection, if the calling application specifies a 
    non-<b>NULL</b> value for the phone-book parameter, <i>lpszPhonebook</i>, 
    the phone-book file must be located in the phone-book directory beneath the all-users application data path. To 
    obtain the correct location for the phone-book file, first call 
    <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha">SHGetFolderPath</a> with a 
    <a href="/windows/desktop/shell/csidl">CSIDL</a> value of <b>CSIDL_COMMON_APPDATA</b>. 
    <b>SHGetFolderPath</b> returns the all-users 
    application data path. Append the following string to this path:

Microsoft\Network\Connections\Pbk

The combined path is the correct location for the phone-book file.

<div class="alert"><b>Note</b>  Specifying a non-<b>NULL</b> value for the <i>lpszPhonebook</i> 
    parameter may not be supported in versions of Windows later than Windows XP.</div>
<div> </div>




> [!NOTE]
> The ras.h header defines RasSetEntryProperties as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)">RASENTRY</a>



<a href="/windows/desktop/api/ras/nf-ras-rascreatephonebookentrya">RasCreatePhonebookEntry</a>



<a href="/windows/desktop/api/ras/nf-ras-rasgetentrypropertiesa">RasGetEntryProperties</a>



<a href="/windows/desktop/api/ras/nf-ras-rasvalidateentrynamea">RasValidateEntryName</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>
