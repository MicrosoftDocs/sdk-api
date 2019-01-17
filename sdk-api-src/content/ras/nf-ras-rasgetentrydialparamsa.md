---
UID: NF:ras.RasGetEntryDialParamsA
title: RasGetEntryDialParamsA function
author: windows-sdk-content
description: The RasGetEntryDialParams function retrieves the connection information saved by the last successful call to the RasDial or RasSetEntryDialParams function for a specified phone-book entry.
old-location: rras\rasgetentrydialparams.htm
tech.root: RRAS
ms.assetid: c6752f95-c7e8-44d9-9dbd-9f03cc4778fa
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RasGetEntryDialParams, RasGetEntryDialParams function [RAS], RasGetEntryDialParamsA, RasGetEntryDialParamsW, _ras_rasgetentrydialparams, ras/RasGetEntryDialParams, ras/RasGetEntryDialParamsA, ras/RasGetEntryDialParamsW, rras.rasgetentrydialparams
ms.topic: function
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasGetEntryDialParamsW (Unicode) and RasGetEntryDialParamsA (ANSI)
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
 - Ext-MS-Win-ras-rasapi32-l1-1-0.dll
 - Ext-MS-Win-ras-rasapi32-l1-1-1.dll
api_name:
 - RasGetEntryDialParams
 - RasGetEntryDialParamsA
 - RasGetEntryDialParamsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RasGetEntryDialParamsA function


## -description


The 
<b>RasGetEntryDialParams</b> function retrieves the connection information saved by the last successful call to the 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> or 
<a href="https://msdn.microsoft.com/e1acd68e-796e-49a2-8c7d-c0fd1a9764ef">RasSetEntryDialParams</a> function for a specified phone-book entry.


## -parameters




### -param arg1 [in]

Pointer to a <b>null</b>-terminated string that specifies the full path and file name of a phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the current default phone-book file. The default phone-book file is the one selected by the user in the <b>User Preferences</b> property sheet of the <i>Dial-Up Networking</i> dialog box. 




<b>Windows Me/98/95:  </b>This parameter should always be <b>NULL</b>. Dial-up networking stores phone-book entries in the registry rather than in a phone-book file.


### -param arg2 [in, out]

Pointer to a 
<a href="https://msdn.microsoft.com/13d15c98-a41b-4bc8-8be6-c0b718b86fea">RASDIALPARAMS</a> structure. 




On input, the <b>dwSize</b> member specifies the size of the 
<a href="https://msdn.microsoft.com/13d15c98-a41b-4bc8-8be6-c0b718b86fea">RASDIALPARAMS</a> structure, and the <b>szEntryName</b> member specifies a valid phone-book entry.

On output, the structure receives the connection parameters associated with the specified phone-book entry.

Note that the <b>szPhoneNumber</b> member of the structure does not receive the phone number associated with the phone-book entry. To get the phone number associated with a phone-book entry, call the 
<a href="https://msdn.microsoft.com/eef9c197-04b3-4f3c-a7bd-8c62f9fac560">RasGetEntryProperties</a> function. If <b>szPhoneNumber</b> is an empty string in the 
<a href="https://msdn.microsoft.com/13d15c98-a41b-4bc8-8be6-c0b718b86fea">RASDIALPARAMS</a> structure passed to 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a>, 
<b>RasDial</b> uses the phone number stored in the phone-book entry.

The <b>szPassword</b> member of the <a href="https://msdn.microsoft.com/13d15c98-a41b-4bc8-8be6-c0b718b86fea">RASDIALPARAMS</a> structure does not return the actual password. Instead,  <b>szPassword</b>  contains a handle to the saved password. Substitute this handle for the saved password in subsequent calls to 
<a href="https://msdn.microsoft.com/e1acd68e-796e-49a2-8c7d-c0fd1a9764ef">RasSetEntryDialParams</a> and 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a>. When presented with this handle, 
<b>RasDial</b>  retrieves and uses the saved password. The value of this handle may change in future versions of the operating system; do not develop code that depends on the contents or format of this value.

<b>Windows NT and Windows Me/98/95:  </b>Secure password feature not supported.


### -param arg3 [out]

Pointer to a flag that indicates whether the function retrieved the password associated with the user name for the phone-book entry. The <i>lpfPassword</i> parameter is <b>TRUE</b> if the system has saved a password for the specified entry. If the system has no password saved for this entry, <i>lpfPassword</i> is <b>FALSE</b>. 




<b>Windows NT and Windows Me/98/95:  </b>The function sets this flag to <b>TRUE</b> if the user's password was returned in the <b>szPassword</b> member of the 
<a href="https://msdn.microsoft.com/13d15c98-a41b-4bc8-8be6-c0b718b86fea">RASDIALPARAMS</a> structure pointed to by <i>lprasdialparams</i>.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> or Winerror.h.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUFFER_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>lprasdialparams</i> or <i>lpfPassword</i> pointer is invalid, or the <i>lprasdialparams</i> buffer is invalid.

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
<dt><b>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</b></dt>
</dl>
</td>
<td width="60%">
The phone-book entry does not exist.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/13d15c98-a41b-4bc8-8be6-c0b718b86fea">RASDIALPARAMS</a>



<a href="https://msdn.microsoft.com/da8bd49f-e890-4e8a-ab4d-7366c6f2b361">RasCreatePhonebookEntry</a>



<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a>



<a href="https://msdn.microsoft.com/7fce1ea8-7ed6-4975-af4b-e20a1c1be5fa">RasEditPhonebookEntry</a>



<a href="https://msdn.microsoft.com/e1acd68e-796e-49a2-8c7d-c0fd1a9764ef">RasSetEntryDialParams</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

