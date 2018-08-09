---
UID: NF:ras.RasSetEntryPropertiesW
title: RasSetEntryPropertiesW function
author: windows-sdk-content
description: The RasSetEntryProperties function changes the connection information for an entry in the phone book or creates a new phone-book entry.
old-location: rras\rassetentryproperties.htm
old-project: rras
ms.assetid: 6532b48b-0d80-4993-800e-c808bb7540d6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RasSetEntryProperties, RasSetEntryProperties function [RAS], RasSetEntryPropertiesA, RasSetEntryPropertiesW, _ras_rassetentryproperties, ras/RasSetEntryProperties, ras/RasSetEntryPropertiesA, ras/RasSetEntryPropertiesW, rras.rassetentryproperties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: RASPROJECTION_INFO_TYPE
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
product: Windows
targetos: Windows
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
req.product: ADAM
---

# RasSetEntryPropertiesW function


## -description


The <b>RasSetEntryProperties</b> function changes the 
    connection information for an entry in the phone book or creates a new phone-book entry.


## -parameters




### -param

TBD




#### - [in]

Pointer to a null-terminated string that specifies the full path and file name of a phone-book (PBK) file. 
      If this parameter is <b>NULL</b>, the function uses the current default phone-book file. 
      The default phone-book file is the one selected by the user in the <b>User Preferences</b> 
      property sheet of the <b>Dial-Up Networking</b> dialog box.


#### - lpszEntry [in]

Pointer to a null-terminated string that specifies an entry name.

If the entry name matches an existing entry, 
       <b>RasSetEntryProperties</b> modifies the properties 
       of that entry.

If the entry name does not match an existing entry, 
       <b>RasSetEntryProperties</b> creates a new 
       phone-book entry. For new entries, call the 
       <a href="https://msdn.microsoft.com/c70ad0d4-6bc1-4716-9a8e-0fbeb55b7560">RasValidateEntryName</a> function to validate the 
       entry name before calling 
       <b>RasSetEntryProperties</b>.


#### - lpRasEntry [in]

Pointer to the <a href="https://msdn.microsoft.com/25c46850-4fb7-47a9-9645-139f0e869559">RASENTRY</a> structure that specifies the 
       new connection data to be associated with the phone-book entry indicated by the 
       <i>lpszEntry</i> parameter.

The caller must provide values for the following members in the 
       <a href="https://msdn.microsoft.com/25c46850-4fb7-47a9-9645-139f0e869559">RASENTRY</a> structure.

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
       member of the <a href="https://msdn.microsoft.com/25c46850-4fb7-47a9-9645-139f0e869559">RASENTRY</a> structure contains the offset to 
       the first string.


#### - dwEntryInfoSize [in]

Specifies the size, in bytes, of the buffer identified by the <i>lpRasEntry</i> 
      parameter.


#### - lpbDeviceInfo [in]

Pointer to a buffer that specifies device-specific configuration information. This is opaque TAPI device 
      configuration information. For more information about TAPI device configuration, see the 
      <a href="_tapi2_linegetdevconfig">lineGetDevConfig</a> function in 
      <a href="_tapi3_telephony_application_programming_interfaces">Telephony Application Programming Interfaces (TAPI)</a> 
      in the Platform SDK.
      

<b>Windows XP:  </b>This parameter is unused. The calling function should set this parameter to 
        <b>NULL</b>.


#### - dwDeviceInfoSize [in]

Specifies the size, in bytes, of the <i>lpbDeviceInfo</i> buffer.
      

<b>Windows XP:  </b>This parameter is unused. The calling function should set this parameter to zero.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from 
       <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> 
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
The <a href="https://msdn.microsoft.com/25c46850-4fb7-47a9-9645-139f0e869559">RASENTRY</a> structure pointed to by the 
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
    <a href="_win32_shgetfolderpath_cpp">SHGetFolderPath</a> with a 
    <a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL</a> value of <b>CSIDL_COMMON_APPDATA</b>. 
    <b>SHGetFolderPath</b> returns the all-users 
    application data path. Append the following string to this path:

Microsoft\Network\Connections\Pbk

The combined path is the correct location for the phone-book file.

<div class="alert"><b>Note</b>  Specifying a non-<b>NULL</b> value for the <i>lpszPhonebook</i> 
    parameter may not be supported in versions of Windows later than Windows XP.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/25c46850-4fb7-47a9-9645-139f0e869559">RASENTRY</a>



<a href="https://msdn.microsoft.com/da8bd49f-e890-4e8a-ab4d-7366c6f2b361">RasCreatePhonebookEntry</a>



<a href="https://msdn.microsoft.com/eef9c197-04b3-4f3c-a7bd-8c62f9fac560">RasGetEntryProperties</a>



<a href="https://msdn.microsoft.com/c70ad0d4-6bc1-4716-9a8e-0fbeb55b7560">RasValidateEntryName</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

