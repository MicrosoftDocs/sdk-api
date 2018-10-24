---
UID: NF:ras.RasGetSubEntryPropertiesW
title: RasGetSubEntryPropertiesW function
author: windows-sdk-content
description: The RasGetSubEntryProperties function retrieves information about a subentry for a specified phone-book entry.
old-location: rras\rasgetsubentryproperties.htm
tech.root: rras
ms.assetid: 6efe7824-54a1-491c-a568-21e23e98ed46
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: RasGetSubEntryProperties, RasGetSubEntryProperties function [RAS], RasGetSubEntryPropertiesA, RasGetSubEntryPropertiesW, _ras_rasgetsubentryproperties, ras/RasGetSubEntryProperties, ras/RasGetSubEntryPropertiesA, ras/RasGetSubEntryPropertiesW, rras.rasgetsubentryproperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasGetSubEntryPropertiesW (Unicode) and RasGetSubEntryPropertiesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasapi32.dll
api_name:
 - RasGetSubEntryProperties
 - RasGetSubEntryPropertiesA
 - RasGetSubEntryPropertiesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RasGetSubEntryPropertiesW function


## -description


The 
<b>RasGetSubEntryProperties</b> function retrieves information about a subentry for a specified phone-book entry.


## -parameters




### -param arg1

TBD


### -param arg2

TBD


### -param arg3

TBD


### -param arg4

TBD


### -param arg5

TBD


### -param arg6

TBD


### -param arg7

TBD




#### - [in]

Pointer to a <b>null</b>-terminated string that specifies the full path and file name of a phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the current default phone-book file. The default phone-book file is the one selected by the user in the <b>User Preferences</b> property sheet of the <b>Dial-Up Networking</b> dialog box. 




<b>Windows Me/98/95:  </b>This parameter should always be <b>NULL</b>. Dial-up networking stores phone-book entries in the registry rather than in a phone-book file.


#### - dwSubEntry [in]

Specifies the one-based index of the subentry.


#### - lpRasSubEntry [in, out]

Pointer to the 
<a href="https://msdn.microsoft.com/48c1b100-e490-41a0-8324-6be2297bd814">RASSUBENTRY</a> structure followed by additional bytes for the alternate phone number list, if there is one. 




On output, the structure receives information about the specified subentry.

On input, the <b>dwSize</b> member specifies the size of the structure. The size identifies the version of the structure. Obtain this size using sizeof(<a href="https://msdn.microsoft.com/48c1b100-e490-41a0-8324-6be2297bd814">RASSUBENTRY</a>).

This parameter can be <b>NULL</b>.


#### - lpbDeviceConfig [in]

Pointer to a TAPI device configuration block. This parameter is currently unused. The caller should pass <b>NULL</b> for this parameter. For more information about TAPI device configuration blocks, see the function 
<a href="_tapi2_linegetdevconfig">lineGetDevConfig</a>.


#### - lpcbDeviceConfig [in]

Pointer to a <b>DWORD</b> that specifies the size of the TAPI device configuration block. This parameter is currently unused. The caller should pass <b>NULL</b> for this parameter.


#### - lpdwcb [in, out]

Pointer to a variable that specifies, on input, the size, in bytes, of the <i>lpRasSubEntry</i> buffer. 




On output, the variable receives the number of bytes returned, or the number of bytes required if the buffer is too small.

This parameter can be <b>NULL</b> if <i>lpRasSubEntry</i> is <b>NULL</b>.


#### - lpszEntry [in]

Pointer to a <b>null</b>-terminated string that specifies the name of an existing entry in the phone book.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> or Winerror.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The function was called with an invalid parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUFFER_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The address or buffer specified by <i>lpRasSubEntry</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpRasSubEntry</i> buffer is too small. The <i>lpdwcb</i> variable receives the required buffer size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_OPEN_PHONEBOOK</b></dt>
</dl>
</td>
<td width="60%">
The phone book is corrupted or is missing components.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</b></dt>
</dl>
</td>
<td width="60%">
The phone-book entry does not exist.

</td>
</tr>
</table>
 




## -remarks



A RAS phone-book entry can have zero or more subentries, each minimally consisting of a device and a phone number. A phone-book entry with multiple subentries can be configured to dial the first available or all subentries when the entry is dialed.

Use the 
<a href="https://msdn.microsoft.com/eef9c197-04b3-4f3c-a7bd-8c62f9fac560">RasGetEntryProperties</a> function to retrieve a 
<a href="https://msdn.microsoft.com/25c46850-4fb7-47a9-9645-139f0e869559">RASENTRY</a> structure containing information about the subentries of a phone-book entry. The <b>dwSubEntries</b> member indicates the number of subentries and the <b>dwDialMode</b> member indicates the dialing configuration.




## -see-also




<a href="https://msdn.microsoft.com/25c46850-4fb7-47a9-9645-139f0e869559">RASENTRY</a>



<a href="https://msdn.microsoft.com/48c1b100-e490-41a0-8324-6be2297bd814">RASSUBENTRY</a>



<a href="https://msdn.microsoft.com/eef9c197-04b3-4f3c-a7bd-8c62f9fac560">RasGetEntryProperties</a>



<a href="https://msdn.microsoft.com/6bbc826b-e296-42d0-89d0-a13d0ce94929">RasSetSubEntryProperties</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

