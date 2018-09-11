---
UID: NF:ras.RasSetEntryDialParamsA
title: RasSetEntryDialParamsA function
author: windows-sdk-content
description: The RasSetEntryDialParams function changes the connection information saved by the last successful call to the RasDial or RasSetEntryDialParams function for a specified phone-book entry.
old-location: rras\rassetentrydialparams.htm
tech.root: RRAS
ms.assetid: e1acd68e-796e-49a2-8c7d-c0fd1a9764ef
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RasSetEntryDialParams, RasSetEntryDialParams function [RAS], RasSetEntryDialParamsA, RasSetEntryDialParamsW, _ras_rassetentrydialparams, dwCallbackId, dwSize, dwSubEntry, ras/RasSetEntryDialParams, ras/RasSetEntryDialParamsA, ras/RasSetEntryDialParamsW, rras.rassetentrydialparams, szCallbackNumber, szDomain, szEntryName, szPassword, szPhoneNumber, szUserName
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
req.unicode-ansi: RasSetEntryDialParamsW (Unicode) and RasSetEntryDialParamsA (ANSI)
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
 - RasSetEntryDialParams
 - RasSetEntryDialParamsA
 - RasSetEntryDialParamsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RasSetEntryDialParamsA function


## -description


The 
<b>RasSetEntryDialParams</b> function changes the connection information saved by the last successful call to the 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> or 
<b>RasSetEntryDialParams</b> function for a specified phone-book entry.


## -parameters




### -param arg1

TBD


### -param arg2

TBD


### -param arg3

TBD




#### - [in]

Pointer to a null-terminated string that specifies the full path and file name of a phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the current default phone-book file. The default phone-book file is the one selected by the user in the <b>User Preferences</b> property sheet of the <b>Dial-Up Networking</b> dialog box. 



						

<b>Windows Me/98/95:  </b>This parameter should always be <b>NULL</b>. Dial-up networking stores phone-book entries in the registry rather than in a phone-book file.


#### - fRemovePassword [in]

Specifies whether to remove the phone-book entry's stored password for the user indicated by <i>lprasdialparams</i>-&gt;<b>szUserName</b>. If <i>fRemovePassword</i> is <b>TRUE</b>, the password is removed. Setting fRemovePassword to <b>TRUE</b> is equivalent to checking the "Unsave Password" check box in Dial-Up Networking. When setting the password or other properties of a phone book entry, set <i>fRemovePassword</i> to <b>FALSE</b>.


#### - lprasdialparams [in]

Pointer to the 
<a href="https://msdn.microsoft.com/13d15c98-a41b-4bc8-8be6-c0b718b86fea">RASDIALPARAMS</a> structure that specifies the connection parameters to be associated with the phone-book entry. 
<b>RasSetEntryDialParams</b> uses the structure's members as follows. 



<table>
<tr>
<th>Member</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="dwSize"></a><a id="dwsize"></a><a id="DWSIZE"></a><dl>
<dt><b><b>dwSize</b></b></dt>
</dl>
</td>
<td width="60%">
Must specify the size of (<a href="https://msdn.microsoft.com/13d15c98-a41b-4bc8-8be6-c0b718b86fea">RASDIALPARAMS</a>) to identify the version of the structure.

</td>
</tr>
<tr>
<td width="40%"><a id="szEntryName"></a><a id="szentryname"></a><a id="SZENTRYNAME"></a><dl>
<dt><b><b>szEntryName</b></b></dt>
</dl>
</td>
<td width="60%">
A null-terminated string that identifies the phone-book entry to set parameters for.

</td>
</tr>
<tr>
<td width="40%"><a id="szPhoneNumber"></a><a id="szphonenumber"></a><a id="SZPHONENUMBER"></a><dl>
<dt><b><b>szPhoneNumber</b></b></dt>
</dl>
</td>
<td width="60%">
Not used. Set to <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="szCallbackNumber"></a><a id="szcallbacknumber"></a><a id="SZCALLBACKNUMBER"></a><dl>
<dt><b><b>szCallbackNumber</b></b></dt>
</dl>
</td>
<td width="60%">
A null-terminated string that contains the callback phone number. If <b>szCallbackNumber</b> is an empty string ( "" ), the callback number is not changed.

</td>
</tr>
<tr>
<td width="40%"><a id="szUserName"></a><a id="szusername"></a><a id="SZUSERNAME"></a><dl>
<dt><b><b>szUserName</b></b></dt>
</dl>
</td>
<td width="60%">
A null-terminated string that contains the logon name of the user associated with this entry. If <b>szUserName</b> is an empty string, the user name is not changed.

</td>
</tr>
<tr>
<td width="40%"><a id="szPassword"></a><a id="szpassword"></a><a id="SZPASSWORD"></a><dl>
<dt><b><b>szPassword</b></b></dt>
</dl>
</td>
<td width="60%">
A null-terminated string that contains the password for the user specified by <b>szUserName</b>. If <b>szUserName</b> is an empty string, the password is not changed. If <b>szPassword</b> is an empty string and <i>fRemovePassword</i> is <b>FALSE</b>, the password is set to the empty string. If <i>fRemovePassword</i> is <b>TRUE</b>, the password stored in this phone-book entry for the user specified by <b>szUserName</b> is removed regardless of the contents of the <b>szPassword</b> string. 




<b>Windows NT 4.0:  </b>The password is changed to the string specified by <b>szPassword</b> regardless of whether <b>szUserName</b> is an empty string.

<b>Windows XP/2000:  </b>If <b>szPassword</b> contains the password handle returned by 
<a href="https://msdn.microsoft.com/37b67845-dd9f-4adc-a33a-f0e5c0bdb6f7">RasGetCredentials</a> or 
<a href="https://msdn.microsoft.com/c6752f95-c7e8-44d9-9dbd-9f03cc4778fa">RasGetEntryDialParams</a>, 
<b>RasSetEntryDialParams</b> returns successfully without changing any currently saved password.

</td>
</tr>
<tr>
<td width="40%"><a id="szDomain"></a><a id="szdomain"></a><a id="SZDOMAIN"></a><dl>
<dt><b><b>szDomain</b></b></dt>
</dl>
</td>
<td width="60%">
A null-terminated string that contains the name of the domain on which to log on. If <b>szDomain</b> is an empty string, the domain name is not changed.

</td>
</tr>
<tr>
<td width="40%"><a id="dwSubEntry"></a><a id="dwsubentry"></a><a id="DWSUBENTRY"></a><dl>
<dt><b><b>dwSubEntry</b></b></dt>
</dl>
</td>
<td width="60%">
Specifies the (one-based) index of the initial subentry to dial when establishing the connection.

</td>
</tr>
<tr>
<td width="40%"><a id="dwCallbackId"></a><a id="dwcallbackid"></a><a id="DWCALLBACKID"></a><dl>
<dt><b><b>dwCallbackId</b></b></dt>
</dl>
</td>
<td width="60%">
Specifies an application-defined value that RAS passes to the 
<a href="https://msdn.microsoft.com/a9395048-492b-42fb-b247-52999cee3f44">RasDialFunc2</a> callback function.

</td>
</tr>
</table>
 


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
The address or buffer specified by <i>lprasdialparams</i> is invalid.

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
 




## -remarks



To create a new phone-book entry, use the 
<a href="https://msdn.microsoft.com/6532b48b-0d80-4993-800e-c808bb7540d6">RasSetEntryProperties</a> function.

<b>Windows XP or later:  </b>Do not use the 
<b>RasSetEntryDialParams</b> function. To set the credentials for a phone-book entry, use the 
<a href="https://msdn.microsoft.com/5ebfffb7-9158-4414-982c-e187600aa1ab">RasSetCredentials</a> function. Set the non-credential members of 
<a href="https://msdn.microsoft.com/13d15c98-a41b-4bc8-8be6-c0b718b86fea">RASDIALPARAMS</a> (for example <b>szCallbackNumber</b>, <b>dwSubEntry</b>, or <b>dwCallbackId</b>) directly in the 
<b>RASDIALPARAMS</b> structure passed as a parameter to the 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> function.




## -see-also




<a href="https://msdn.microsoft.com/13d15c98-a41b-4bc8-8be6-c0b718b86fea">RASDIALPARAMS</a>



<a href="https://msdn.microsoft.com/da8bd49f-e890-4e8a-ab4d-7366c6f2b361">RasCreatePhonebookEntry</a>



<a href="https://msdn.microsoft.com/7fce1ea8-7ed6-4975-af4b-e20a1c1be5fa">RasEditPhonebookEntry</a>



<a href="https://msdn.microsoft.com/c6752f95-c7e8-44d9-9dbd-9f03cc4778fa">RasGetEntryDialParams</a>



<a href="https://msdn.microsoft.com/5ebfffb7-9158-4414-982c-e187600aa1ab">RasSetCredentials</a>



<a href="https://msdn.microsoft.com/6532b48b-0d80-4993-800e-c808bb7540d6">RasSetEntryProperties</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

